---
nav_title: ページ
article: Pages
description: "Braze Docs でページを作成、変更、削除する方法について説明します。"
page_order: 0
noindex: true
---

# ページ

> Braze Docs でページを作成、変更、削除する方法について説明します。セクションを作成または順序変更するには、[セクション]({{site.baseurl}}/contributing/content_management/sections/)を参照してください。ページの一般的な情報については、[Content Management]({{site.baseurl}}/contributing/content_management/#pages)を参照してください。

{% multi_lang_include contributing/prerequisites.md %}

## ページの作成

### ステップ 3新しいファイルを作成する

関連するディレクトリを開き、ページの新しいMarkdown ファイルを作成します。

```bash
PAGE_TITLE.md
```

`PAGE_TITLE` をページのタイトルに置き換えます。これは[Braze Docs Style Guide]({{site.baseurl}}/contributing/style_guide/) の後に続きます。すべての小文字を使用し、特殊文字を削除し、スペースをアンダースコアに置き換えます(`_`)。ファイル名は次のようになります。

- **ページtitle:** C++ の開発環境の設定
- **ファイル name:** `setting_up_your_development_environment_for_cpp.md`

{% multi_lang_include contributing/alerts/tip_locating_a_file.md %}

### ステップ 3テンプレートの追加

次のテンプレートのいずれかを Markdown ファイルにコピーアンドペーストします。詳細については、[テンプレート]({{site.baseurl}}/contributing/templates/)を参照してください。

#### 基本テンプレート

{% multi_lang_include contributing/templates/basic.md %}

#### 技術パートナーテンプレート

{% multi_lang_include contributing/templates/technology_partner.md %}

## 書き込み内容

このセクションで説明するブレーズ固有の構文以外のすべてのコンテンツは、[標準のMarkdown 構文](https://www.markdownguide.org/basic-syntax/) を使用して記述します。

### 相互参照

Braze Docs 以外でホストされているページを参照するには、標準のMarkdown 構文を使用します。

{% raw %}
```markdown
[LINK_TEXT](FULL_URL)
```
{% endraw %}

Braze Docs でホストされているページを相互参照するには、次のBraze 固有の構文を使用します。

{% raw %}
```markdown
[LINK_TEXT]({{site.baseurl}}/SHORT_URL)
```
{% endraw %}

{% alert note %}
フルウォークスルーについては、[相互参照]({{site.baseurl}}/contributing/content_management/cross_referencing/)を参照してください。
{% endalert %}

### 画像を追加する

イメージを追加するには、イメージのPNG ファイルを`assets/img` 内の該当する場所に配置し、次の構文を使用します。

{% raw %}
```markdown
![ALT_TEXT.]({% image_buster /assets/img/DIRECTORY/IMAGE.png %})
```
{% endraw %}

{% alert note %}
フルウォークスルーについては、[新しいイメージの追加]({{site.baseurl}}/contributing/content_management/images/)を参照してください。
{% endalert %}
