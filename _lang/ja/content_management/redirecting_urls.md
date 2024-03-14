---
nav_title: URLをリダイレクトする
article: Redirecting URLs
description: "Braze Docsのページとページ見出しのURLをリダイレクトする方法を学ぶ。"
page_order: 6
noindex: true
---

# URLをリダイレクトする

> Braze Docsのページとページ見出しのURLをリダイレクトする方法を学ぶ。

ページURLは常にBraze Docsリポジトリのディレクトリ構造と一致する。Markdownファイルの名前が変更されたり、別のディレクトリに移動された場合、リダイレクトが設定されていないと、元のURLは404エラーになる。

![Example of a 404 page on Braze Docs.]({% image_buster /assets/img/contributing/styling_examples/404.png %})

URLリダイレクトを設定することで、ユーザーのブックマークが壊れるのを防ぐことができる。

{% multi_lang_include contributing/prerequisites.md %}

## ページをリダイレクトする

ページのURLをBraze Docsのホームページまたは新しい場所にリダイレクトすることができる。

{% tabs local %}
{% tab home page %}
関連するMarkdownファイルを開き、YAMLフロントマターに以下のキーと値のペアを追加する。すでに`layout` キーがある場合は、既存のキーを新しいキーに置き換える。

マークダウン
---
layout: blank\_config
---
\`\`\`

あなたのYAMLフロント・マターは以下のようなものでなければならない：

マークダウン
---
nav_title: カスタマイズガイド
config_only: 真の
layout: blank\_config
04
---
\`\`\`
{% endtab %}

{% tab new location %}
関連するMarkdownファイルを移動またはリネームしたら、`assets/js/` ディレクトリに移動し、グローバル・リダイレクト・ファイルを開く。

```bash
braze-docs
└── assets
    └── js
        └── broken_redirect_list.js
```

ファイルの先頭で、以下の構文を使って新しい行にリダイレクトを作成する：

```javascript
validurls['REDIRECT_FROM'] = 'REDIRECT_TO';
```

以下を交換する：

| プレースホルダー
|-----------------|------------------------------------------------------------------------------------------------|
|`REDIRECT_FROM` | URL文字列から`https://www.braze.com/` を削除したリダイレクト_先の_URL。|
|`REDIRECT_TO` | URL文字列から`https://www.braze.com/` を削除したリダイレクト_先の_URL。   |
{: .reset-td-br-1 .reset-td-br-2}

{% multi_lang_include contributing/alerts/warning_urls_must_be_lowercase.md %}

リダイレクトは以下のようなものであるべきだ：

```javascript
validurls['/docs/user_guide/data_and_analytics/engagement_reports'] = '/docs/user_guide/data_and_analytics/your_reports/engagement_reports';
```
{% endtab %}
{% endtabs %}

## 見出しをリダイレクトする

ページ内の見出しのURLをリダイレクトするには、ページのYAMLフロントマター内で`local_redirect` キーを使う。最初に、関連するMarkdownファイルを移動するか名前を変更し、ページのYAMLフロントマターで次の構文を使う：

```
local_redirect:
  OLD_HEADING: 'NEW_HEADING_URL'
```

以下を交換する：

| プレースホルダー
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
｜`OLD_HEADING` ｜`#` を削除した[Markdown構文の](https://www.markdownguide.org/basic-syntax/#an-example-putting-the-parts-together)古い見出し。|
|`NEW_HEADING_URL` | URL文字列から`https://www.braze.com/` を削除した、リダイレクト_さ_せたい新しい見出しURL。                                      |
{: .reset-td-br-1 .reset-td-br-2}

{% multi_lang_include contributing/alerts/warning_urls_must_be_lowercase.md %}

リダイレクトは以下のようなものであるべきだ：

ヤムル
---
nav_title: はじめに
article_title: Braze SDKを使い始める
description: "Braze SDKを初めて使う人は、始め方を学ぼう。"
local\_redirectである：
  building-from-source: '/docs/developer_guide/getting_started/#using-our-install-script'
\`\`\`
