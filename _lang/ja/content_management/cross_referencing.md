---
nav_title: 相互参照
article: Cross-referencing
description: "Braze Docsの他のページを相互参照する方法をご覧ください。"
page_order: 4
noindex: true
---

# 相互参照

> Braze Docsの他のページを相互参照する方法をご覧ください。Braze Docs外のページを相互参照するには、[標準のMarkdown構文](https://www.markdownguide.org/basic-syntax/#links)を使用します。

{% multi_lang_include contributing/prerequisites.md %}

## 相互参照を作成する

相互参照を作成する場合、インライン方式または参照スタイル方式のいずれかを使用できます。インライン方式はわかりやすさを優先し、参照スタイル方式は読みやすさを優先します。

{% tabs %}
{% tab in-line %}
関連するMarkdownファイルを開き、インラインリンクを作成します。

{% subtabs %}
{% subtab Markdown %}

{% raw %}
```markdown
[LINK_TEXT]({{site.baseurl}}/SHORT_URL)
```
{% endraw %}

次のように置き換えます。

|プレースホルダ|説明|
|-------------|----------------------------------------------------|
|`LINK_TEXT`|ページタイトルまたは関連するアクション。|
| `SHORT_URL` | `https://www.braze.com`を削除したページのURL。 |
{: .reset-td-br-1 .reset-td-br-2}

インラインリンクは次のようになります。

{% raw %}
```markdown
Before continuing, [create your SSH token]({{site.baseurl}}/docs/developer_guide/platform_wide/sdk_authentication).
```
{% endraw %}
{% endsubtab %}

{% subtab HTML %}

{% raw %}
```markdown
<a href='[SHORT_URL]'>[LINK_TEXT]</a>
```
{% endraw %}

次のように置き換えます。

|プレースホルダ|説明|
|-------------|----------------------------------------------------|
|`LINK_TEXT`|ページタイトルまたは関連するアクション。|
| `SHORT_URL` | `https://www.braze.com`を削除したページのURL。 |
{: .reset-td-br-1 .reset-td-br-2}

インラインリンクは次のようになります。

{% raw %}
```markdown
To learn about the different custom attribute data types you can use to segment users, view <a href="/docs/user_guide/data_and_analytics/custom_data/custom_attributes/#custom-attribute-data-types">Custom attribute data types</a>.
```
{% endraw %}
{% endsubtab %}
{% endsubtabs %}

{% endtab %}

{% tab reference-style %}
関連するMarkdownファイルを開き、参照スタイルのリンクを作成します。

```markdown
[LINK_TEXT][REFERENCE_NUMBER]
```

次のように置き換えます。

|プレースホルダ|説明|
|--------------------|--------------------------------------------------------------------------|
|`LINK_TEXT`|ページタイトルまたは関連するアクション。|
|`REFERENCE_NUMBER`|このページの他の参照スタイルのリンクにまだ割り当てられていない正の整数を割り当てます。|
{: .reset-td-br-1 .reset-td-br-2}

リファレンスは次のようになります。

```markdown
Before continuing, [create your SSH token][2]. When you're finished, see [Step 2: Uploading your token][5].
```

ページの下部に、関連するリンクを追加します。

{% raw %}
```markdown
[REFERENCE_NUMBER]: {{site.baseurl}}SHORT_URL
```
{% endraw %}

次のように置き換えます。

|プレースホルダ|説明|
|--------------------|---------------------------------------------------------|
|`REFERENCE_NUMBER`|リンクする参考文献の番号。|
| `SHORT_URL` | `https://www.braze.com/docs`を削除したページのURL。 |
{: .reset-td-br-1 .reset-td-br-2}

リンクは次のようになります。

{% raw %}
```markdown
[2]: {{site.baseurl}}/developer_guide/platform_wide/sdk_authentication/
[5]: {{site.baseurl}}/developer_guide/platform_wide/swift#step-2-uploading-your-token
```
{% endraw %}
{% endtab %}
{% endtabs %}
