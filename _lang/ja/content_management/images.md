---
nav_title: 画像
article: Images
description: "Braze Docsで画像を追加、修正、削除する方法を説明します。"
page_order: 2
noindex: true
---

# 画像

> Braze Docsで画像を追加、修正、削除する方法を説明します。イメージに関する一般的な情報については、「[コンテンツ管理]({{site.baseurl}}/contributing/content_management/#images)」を参照してください。

{% multi_lang_include contributing/prerequisites.md %}

## 新しいイメージを追加する

### ステップ 3イメージファイルを追加します

テキストエディタで、「`assets`」>「`img`」を開きます。通常、新しい画像はページの他の画像と同じディレクトリに追加する必要があります。ただし、最善の判断で行ってください。新しい画像が[Braze Docsスタイルガイド]({{site.baseurl}}/contributing/style_guide/)に従っていることを確認し、関連するサブディレクトリにPNGファイルを追加します。

```bash
braze-docs
└── assets
    └── img
        └── DIRECTORY
            └── FILE.png
```

次のように置き換えます。

|プレースホルダ|説明|
|-------------|-------------------------------------------------------------------------------------------|
| `DIRECTORY` | 関連するディレクトリの名前。該当するディレクトリがない場合は作成してもよい。|
| `FILE` | ファイル拡張子を含むファイル名。 |
{: .reset-td-br-1 .reset-td-br-2}

イメージファイルは次のようになります。

```bash
braze-docs
└── assets
    └── img
        └── contributing 
            └── github_home_page.png
```

### ステップ 3画像へのリンク

新しい画像にリンクするときは、インラインまたは参照スタイルの構文を使用できます。インライン構文は明確さを優先し、参照スタイルの構文は可読性を優先します。

{% tabs local %}
{% tab in-line %}
Markdownファイルで、インライン構文を使用して新しい画像にリンクします。

{% raw %}
```markdown
![ALT_TEXT.]({% image_buster /assets/img/DIRECTORY/IMAGE.png %})
```
{% endraw %}

次のように置き換えます。

|プレースホルダ|説明|
|-------------|-------------------------------------------------------------------------------------------------------------------------|
| `ALT_TEXT` | 画像の代替テキスト。これは、スクリーンリーダーを使用しているユーザーがBlaze Docsに等しくアクセスできるようにするために必要です。|
| `IMAGE` | `img`ディレクトリから始まる画像への相対パス。 |
{: .reset-td-br-1 .reset-td-br-2}

インラインイメージは次のようになります。

{% raw %}
```markdown
![The form for creating a new pull request on GitHub.]({% image_buster /assets/img/contributing/getting_started/github_pull_request.png %})
```
{% endraw %}
{% endtab %}

{% tab reference-style %}
Markdownファイルで、参照スタイルの構文を使用して新しい画像にリンクします。

{% raw %}
```markdown
![ALT_TEXT.][REFERENCE_NUMBER]
```
{% endraw %}

次のように置き換えます。

|プレースホルダ|説明|
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| `ALT_TEXT` | 画像の代替テキスト。これは、スクリーンリーダーを使用しているユーザーがBlaze Docsに等しくアクセスできるようにするために必要です。|
|`REFERENCE_NUMBER`|このページの他の参照スタイルのリンクにまだ割り当てられていない正の整数を割り当てます。|
{: .reset-td-br-1 .reset-td-br-2}

インラインイメージは次のようになります。

{% raw %}
```markdown
![The form for creating a new pull request on GitHub.][10]
```
{% endraw %}

ページの下部に、参照を追加します。

{% raw %}
```markdown
[REFERENCE_NUMBER]: {{site.baseurl}}SHORT_URL
```
{% endraw %}

次のように置き換えます。

|プレースホルダ|説明|
|--------------------|---------------------------------------------------------|
|`REFERENCE_NUMBER`|リンクする参考文献の番号。|
| `IMAGE` | `img`ディレクトリから始まる画像への相対パス。 |
{: .reset-td-br-1 .reset-td-br-2}

リンクは次のようになります。

{% raw %}
```markdown
[10]: {% image_buster /assets/img/contributing/getting_started/github_pull_request.png %}
```
{% endraw %}
{% endtab %}
{% endtabs %}

## イメージを更新する

### ステップ 3元のリファレンスを見つける

関連するMarkdownファイルを開き、古い[インライン]({{site.baseurl}}/contributing/content_management/images/?tab=in-line#step-2-link-to-the-image)または[参照スタイル]({{site.baseurl}}/contributing/content_management/images/?tab=reference-style#step-2-link-to-the-image)の画像リンクを探します。リンクは次のようになります。

{% raw %}
```markdown
{% image_buster /assets/img/DIRECTORY/IMAGE.png %}
```
{% endraw %}

### ステップ 3画像の更新

既存のイメージを更新する場合、新しいイメージファイルを追加するか、既存のイメージファイルを置き換えることができます。新しい画像が[Braze Docsスタイルガイド]({{site.baseurl}}/contributing/style_guide/)に従っていることを確認してください。

- **既存のファイルを上書き(推奨):**この方法は、元の画像は正確な内容を描写しているが、古いブランディングが描写されている画像など、視覚的に古い場合に使用します。この方法では、Blaze Docsリポジトリに保存される画像の総数を減らすことができます。
- **新しいファイルを追加します:**この方法は、廃止予定の機能やワークフローが描かれた画像など、元の画像が完全に古いコンテンツを示している場合に使用します。

{% tabs local %}
{% tab overwrite existing file %}
新しいイメージの名前を元のイメージの名前に合わせて変更します。次の例では、イメージファイル名がどのように同一であるかを確認します。

- **オリジナルファイルname:**`getting_started_with_github_select_start3.png`
- **新しいファイルname:**`getting_started_with_github_select_start3.png`

次に、新しい画像を元の画像と同じディレクトリに追加します。イメージの上書きを確認するメッセージが表示されたら、イメージファイルは次のようになります。

```bash
braze-docs
└── assets
    └── img
        └── contributing 
            └── getting_started_with_github_select_start3.png
```
{% endtab %}

{% tab add new file%}
通常、新しい画像はこのページの他の画像と同じディレクトリに追加する必要がありますが、最善の判断で追加してください。準備ができたら、`assets/img/`内の該当する場所にPNGファイルを追加します。

{% alert warning %}
新しいイメージファイルを追加するときは、古いイメージファイルを削除しないでください。
{% endalert %}

```bash
braze-docs
└── assets
    └── img
        └── DIRECTORY
            └── FILE.png
```

次のように置き換えます。

|プレースホルダ|説明|
|-------------|-------------------------------------------------------------------------------------------|
| `DIRECTORY` | 関連するディレクトリの名前。該当するディレクトリがない場合は作成してもよい。|
| `FILE` | ファイル拡張子を含むファイル名。 |
{: .reset-td-br-1 .reset-td-br-2}

イメージファイルは次のようになります。

```bash
braze-docs
└── assets
    └── img
        └── contributing 
            └── github_home_page.png
```

画像を関連ディレクトリに追加したら、[インライン]({{site.baseurl}}/contributing/content_management/images/?tab=in-line#step-2-link-to-the-image)または[参照スタイル]({{site.baseurl}}/contributing/content_management/images/?tab=reference-style#step-2-link-to-the-image)の構文を使用してこの画像にリンクできます。
{% endtab %}
{% endtabs %}

## イメージを削除する

画像を削除するには、関連するMarkdownファイルを開いて、[インライン]({{site.baseurl}}/contributing/content_management/images/?tab=in-line#step-2-link-to-the-image)または[参照スタイル]({{site.baseurl}}/contributing/content_management/images/?tab=reference-style#step-2-link-to-the-image)の画像リンクを削除します。リポジトリからイメージファイルを削除しないでください。

{% alert warning %}
画像ファイルが削除されると、他のBlaze Docs言語の翻訳ではその画像が壊れます。
{% endalert %}
