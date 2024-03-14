---
nav_title: メタデータ
article: Metadata
description: "これらは、ページのYAMLフロントマターに追加できるメタデータキーです。"
page_order: 0
noindex: true
---

#  メタデータ

> これらは、ページのYAMLフロントマターに追加できるメタデータキーです。一般的な情報については、「[コンテンツ管理]({{site.baseurl}}/contributing/content_management/#pages)」を参照してください。

Markdownファイルにメタデータを追加するには、ファイルの先頭にJekyllのフロントマター構文を追加する必要があります。

\`\`\`マークダウン
---
メタデータキー:メタデータ\_値
---

# Braze ドキュメントを使い始める

Braze Docs または Docs-as-code を初めて使用する場合は、チュートリアルから始めてください。
\`\`\`

以下を置き換えてください。

| プレースホルダー | 説明 |
|------------------|---------------------------------------------------------------------------------------------------------------------------|
| `METADATA_KEY` | サポートされているメタデータ型を表すキー。[次のセクションのメタデータキーに置き換えてください](#required-keys)。|
| `METADATA_VALUE` | メタデータキーに割り当てられた値。次のセクションでメタデータキーがサポートされている値を確認してください。|
{: .reset-td-br-1 .reset-td-br-2}

## 必要なキー

### 記事タイトル

`article_title`このキーは、オンライン検索結果のページタイトルとエンドユーザーのブラウザタブを設定するために使用されます。`string`このキーは任意の値を受け入れます。命名規則については、[Braze Docs]({{site.baseurl}}/contributing/style_guide/) スタイルガイドをご覧ください。

{% tabs local %}
{% tab usage example %}
\`\`\`マークダウン
---
article_title: Braze ドキュメントを使い始める
---
\`\`\`
{% endtab %}
{% endtabs %}

### [説明]

`description`このキーは、オンライン検索結果のページ説明を設定するために使用されます。このキーは、二重引用符で囲まれた 150 `string` 文字未満の値であれば何でも受け入れます。

{% tabs local %}
{% tab usage example %}
\`\`\`マークダウン
---
description: 「Braze Docs を初めて使用する場合は、このステップバイステップのチュートリアルから始めてください。」
---
\`\`\`
{% endtab %}
{% endtabs %}

### ナビゲーションタイトル

`nav_title`このキーは、Braze Docsの左側のナビゲーションバーのページタイトルを設定するために使用されます。このキーは 30 `string` 文字未満で入力できます。[`hidden`](#hide-page-from-navigation)`nav_title`キーがに設定されている場合`true`、は必要ありません。

{% tabs local %}
{% tab usage example %}
\`\`\`マークダウン
---
nav_title: はじめに
---
\`\`\`
{% endtab %}
{% endtabs %}

## オプションキー

### エンゲージメントツール

`tool`このキーは、ページの関連するエンゲージメントツールを設定するために使用されます。このキーは、次の 1 `string` つまたは複数の値をリストとして受け入れます。

- `dashboard`
- `docs`
- `canvas`
- `campaigns`
- `currents`
- `location`
- `media`
- `reports`
- `segments`
- `templates`

{% tabs local %}
{% tab usage example %}
\`\`\`マークダウン
---
tool:
  -電流
  -セグメント
---
\`\`\`
{% endtab %}
{% endtabs %}

### ナビゲーションからページを非表示にする

`hidden`このキーは、Braze Docsの左側のナビゲーションからページを非表示にするために使用されます。`true`このキーはブーリアン値またはを受け入れます。`false`

{% tabs local %}
{% tab usage example %}
\`\`\`マークダウン
---
hidden: 本当
---
\`\`\`
{% endtab %}
{% endtabs %}

### 検索からページを非表示にする

`noindex`このキーは、内部および外部の検索結果（Braze DocsやGoogle検索など）からページを非表示にするために使用されます。`true`このキーはブーリアン値またはを受け入れます。`false`

{% tabs local %}
{% tab usage example %}
\`\`\`マークダウン
---
noindex: 本当
---
\`\`\`
{% endtab %}
{% endtabs %}

### 目次を非表示にする

`hide_toc`このキーは、ページの右側にあるページ内の目次 (TOC) を非表示にするために使用されます。`true`このキーはブーリアン値またはを受け入れます。`false`

{% tabs local %}
{% tab usage example %}
\`\`\`マークダウン
---
hide_toc: 本当
---
\`\`\`
{% endtab %}
{% endtabs %}

### 目次の見出しを非表示にする

`toc_headers`このキーは、ページの右側にあるページ内の目次 (TOC) から同じレベルのすべての見出しを非表示にするために使用されます。このキーは以下の文字列値を受け入れます。

- `h1`
- `h2`
- `h3`
- `h4`

`toc_headers` 割り当てられた値と一致するすべての見出しが非表示になります。目次から特定の見出しを非表示にすることはできません。

{% tabs local %}
{% tab usage example %}
\`\`\`マークダウン
---
目次ヘッダー:h2
---
\`\`\`
{% endtab %}
{% endtabs %}

### Braze のメッセージングチャンネル

`channel`このキーは、ページの関連するメッセージングチャネルを設定するために使用されます。このキーは、次の 1 `string` つまたは複数の値をリストとして受け入れます。

- `content cards`
- `email`
- `in-app messages`
- `news feed`
- `push`
- `sms`
- `webhooks`

{% tabs local %}
{% tab usage example %}
\`\`\`マークダウン
---
チャネル:
  メール
  -ニュースフィード
---
\`\`\`
{% endtab %}
{% endtabs %}

### ナビゲーションのみ

`config_only`このキーは、ページのコンテンツを左側のナビゲーションバーに隠さずに非表示にするために使用されます。このキーは、[ランディングページのないセクションを作成するときに使用します]({{site.baseurl}}/contributing/content_management/sections?tab=without%20landing%20page#step-2-configure-your-section)。`true`このキーはブーリアン値またはを受け入れます。`false`

{% tabs local %}
{% tab usage example %}
\`\`\`マークダウン
---
config_only: 本当
---
\`\`\`
{% endtab %}
{% endtabs %}

### デフォルト URL を上書き

`permalink`キーをキーと一緒に使用すると[`hidden`](#hide-page-from-navigation)、Braze Docs のページのデフォルト URL が上書きされます。に代入された値は、`permalink``https://www.braze.com/docs`リダイレクトの前に付加されます。このキーは、`string`次の要件を満たす任意の値を受け入れます。

- 文字は小文字です
- 単語はアンダースコア () `_` で区切られています
- 「ディレクトリ」はフォワードスラッシュ () `/` で区切られています
- その他の特殊文字はすべて削除されます

{% tabs local %}
{% tab usage example %}
\`\`\`マークダウン
---
hidden: 本当
permalink: /support_contact/docs_team/
---
\`\`\`
{% endtab %}
{% endtabs %}

### ページレイアウト

`layout`キーはページのレイアウトを設定するために使用されます。`layout`設定されていない場合は、`default`レイアウトが使用されます。`string`このキーは以下の値のいずれかを受け入れます。

- `api_page`
- `dev_guide`
- `featured_video`
- `featured`
- `glossary_page`
- `blank_config`
- `redirect`

各値の詳細については、「[ページレイアウト]({{site.baseurl}}/contributing/yaml_front_matter/page_layouts/)」を参照してください。

{% tabs local %}
{% tab usage example %}
\`\`\`マークダウン
---
page_layout: 用語集ページ
---
\`\`\`
{% endtab %}
{% endtabs %}

### ページ順序

`page_order`このキーは、[左側のナビゲーションバーのセクションを並べ替えるために使用されます]({{site.baseurl}}/contributing/content_management/sections/#ordering-a-section)。このキーは、負でない任意の数 (`0`、`20`、など`5.5`) を受け入れます。

{% tabs local %}
{% tab usage example %}
\`\`\`マークダウン
---
04
---
\`\`\`
{% endtab %}
{% endtabs %}

### ページタイプ

`page_type`キーはページのフォーマットを設定するために使用されます。`string`このキーは以下の値のいずれかを受け入れます。

- `glossary`
- `solution`
- `reference`
- `tutorial`
- `landing`
- `partner`
- `update`

各値の詳細については、「[ページタイプ]({{site.baseurl}}/contributing/yaml_front_matter/page_layouts/)」を参照してください。

{% tabs local %}
{% tab usage example %}
\`\`\`マークダウン
---
page_type: チュートリアル
---
\`\`\`
{% endtab %}
{% endtabs %}

### プラットフォーム

`platform`このキーは、ページの関連プラットフォームを設定するために使用されます。このキーは、1 つ以上の [Braze SDK `string` をリストの値として受け入れます]({{site.baseurl}}/developer_guide/home/)。

{% tabs local %}
{% tab usage example %}
\`\`\`マークダウン
---
プラットフォーム:
  -iOS
  -ウェブ
  Android 29.0.1+
---
\`\`\`
{% endtab %}
{% endtabs %}
