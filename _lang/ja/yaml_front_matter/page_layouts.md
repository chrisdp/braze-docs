---
nav_title: ページレイアウト
article: Page layouts
description: "これらはページのYAMLフロントマターで`page_layout`キーに割り当てることができるページレイアウトです。"
page_order: 2
noindex: true
---

#  ページレイアウト

> これらは、ページのYAMLフロントマターで[`page_layout`]({{site.baseurl}}/contributing/yaml_front_matter/metadata/#page-layout)キーに割り当てることができるページレイアウトです。より一般的な情報については、「[コンテンツ管理]({{site.baseurl}}/contributing/content_management/#layouts)」を参照してください。

## 前提条件

ページレイアウトを使用するには、YAMLフロントマターに[`page_layout`]({{site.baseurl}}/contributing/yaml_front_matter/metadata/#page-layout)キーを追加する必要があります。

\`\`マークダウン
---
nav_title: はじめに
article_title: Braze Docsの使い方
page_layout: PAGE\_LAYOUT\_VALUE
---
\`\`\`

`PAGE_LAYOUT_VALUE`は、次のセクションのいずれかの値に置き換えてください。

## ビジュアルレイアウト

### APIページ

`api_page`値はAPIページ形式の適用に使用します。次の例では、この形式が[リスト統合]({{site.baseurl}}/api/endpoints/cdi/get_integration_list/)ページに適用されます。

{% tabs local %}
{% tab example output %}
![An example page using the 'api_page' layout.]({% image_buster /assets/img/contributing/styling_examples/layouts/api_page.png %})
{% endtab %}
{% endtabs %}

### 開発者ガイド

`dev_guide`値は、開発者ガイドの形式を適用するために使用されます。次の例では、この形式を[カタログエンドポイント]({{site.baseurl}}/api/endpoints/catalogs)ページに適用しています。 

{% tabs local %}
{% tab example output %}
![An example page using the 'dev_guide' layout.]({% image_buster /assets/img/contributing/styling_examples/layouts/dev_guide.png %})
{% endtab %}
{% endtabs %}

### 注目ページ

`featured`値は、アイキャッチページの書式を適用するために使用されます。次の例では、この形式が[予測イベント]({{site.baseurl}}/user_guide/sage_ai/predictive_suite/predictive_events)ページに適用されます。

{% tabs local %}
{% tab example output %}
![An example page using the 'featured' layout.]({% image_buster /assets/img/contributing/styling_examples/layouts/featured.png %})
{% endtab %}
{% endtabs %}

### 用語集ページ

`glossary_page`値は、用語集のページ形式を適用するために使用します。次の例では、この形式が「[プッシュ通知の種類]({{site.baseurl}}/user_guide/message_building_by_channel/push/types)」ページに適用されます。

{% tabs local %}
{% tab example output %}
![An example page using the 'glossary_page' layout.]({% image_buster /assets/img/contributing/styling_examples/layouts/glossary_page.png %})
{% endtab %}
{% endtabs %}

{% alert tip %}
特定のレイアウトでは、`"guide_top_text:"`のような値はMarkdownのフォーマットを持つと恩恵を受ける場合があります。特定のYAML値に対してMarkdownフォーマットを使用できます。これを行うには、YAMLの値として`>`を追加し、その後にテキストをインデントします。
<br>
例えば、<br>
guide\_top\_text: ><br>
    \#これはMarkdownのフォーマット例です
{% endalert %}

## その他のレイアウト

### 空白の設定

`blank_config`値は、Blaze Docsでページを非表示にし、ユーザーを自動的に`www.braze.com/docs`にリダイレクトするために使用します。詳細については、「[URLのリダイレクト]({{site.baseurl}}/contributing/content_management/redirecting_urls/?tab=home%20page#redirecting-a-page)」を参照してください。

### リダイレクト

`redirect`値は、ページ内見出しのURLをリダイレクトするために使用されます。詳しくは、 [URLのリダイレクト]({{site.baseurl}}/contributing/content_management/redirecting_urls/#redirecting-a-heading) を参照してください。
