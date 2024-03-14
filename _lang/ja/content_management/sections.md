---
nav_title: セクション
article: Sections
description: "Braze Docsでセクションを作成して注文する方法を説明します。"
page_order: 2
noindex: true
---

# セクション

> Braze Docsでセクションを作成して注文する方法を説明します。代わりに個別のページを作成、変更、または削除するには、[「ページ」]({{site.baseurl}}/contributing/content_management/pages/)を参照してください。セクションに関する一般的な情報については、「[コンテンツ管理]({{site.baseurl}}/contributing/content_management/#sections)」を参照してください。

{% multi_lang_include contributing/prerequisites.md %}

## セクションの作成

### ステップ 3ディレクトリとMarkdownファイルを作成する

関連するプライマリセクションまたはサブセクションを開き、新しいセクション用のディレクトリとMarkdownファイルを作成します。

```plaintext
braze-docs
└── _docs
    └── PRIMARY_SECTION 
        └── SUBSECTION 
            ├── NEW_DIRECTORY 
            └── NEW_FILE.md
```

次のように置き換えます。

|プレースホルダ|説明|
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `PRIMARY_SECTION` | 新しいコンテンツが属するプライマリセクションの名前。詳細については、「[プライマリ」セクション]({{site.baseurl}}/contributing/content_management/#primary-sections)を参照してください。 |
| `SUBSECTION` | 該当する場合、新しいコンテンツが属するサブセクションの名前。詳細については、「[サブセクション]({{site.baseurl}}/contributing/content_management/#subsections)」を参照してください。 |
| `NEW_DIRECTORY` | 新しいセクションの名前。[Braze Docsスタイルガイド]({{site.baseurl}}/contributing/style_guide/)に従う必要があります。すべて小文字を使用し、特殊文字を削除し、スペースをアンダースコア（`_`）に置き換えます。この名前は`NEW_FILE`と一致している必要があります。|
| `NEW_FILE` | 新しいセクションの名前。[Braze Docsスタイルガイド]({{site.baseurl}}/contributing/style_guide/)に従う必要があります。すべて小文字を使用し、特殊文字を削除し、スペースをアンダースコア（`_`）に置き換えます。この名前は`NEW_DIRECTORY`と一致している必要があります。|
{: .reset-td-br-1 .reset-td-br-2}

ディレクトリ構造は次のようになります。

```plaintext
braze-docs
└── _docs
    └── _developer_guide 
        └── platform_wide 
            ├── getting_started 
            └── getting_started.md
```

### ステップ 3セクションを構成する

新しいセクションを作成する場合、ランディングページの有無を設定できます。

- **ランディングページ付き：**「はじめに」セクションのランディングページに前提条件を列挙し、ユーザージャーニーの概要を説明するなど、セクションに専用の概要が必要な場合にこの方法を使用します。
- **ランディングページを使用しない場合：**この方法は、セクションに専用の概要が不要な場合に使用します。[Braze Docsスタイルガイド]({{site.baseurl}}/contributing/style_guide/)に記載されているように、コンテンツは常に役に立つものであるべきです。そのため、有益なコンテンツがほとんど提供されない場合は、ランディングページの追加は避けてください。

{% tabs %}
{% tab with landing page %}
新しいMarkdownファイルを開き、以下のテンプレートを追加します。その他のテンプレートについては、「[テンプレート]({{site.baseurl}}/contributing/templates/)」を参照してください。

\`\`マークダウン
---
nav_title: NAV\_TITLE
article_title: LANDING\_PAGE\_TITLE
description: SHORT\_DESCRIPTION
---

# LANDING\_PAGE\_TITLE 

> SHORT\_DESCRIPTION

## HEADING

コンテンツ
\`\`\`

次のように置き換えます。

|プレースホルダ|説明|
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`NAV_TITLE`|左側のナビゲーションバーに表示されるページのタイトル。ほとんどの場合、`nav_title`は`article_title`に一致する必要があります。ただし、スペースを節約するために、短く_ても類似_のタイトルを使用してもかまいません。|
|`LANDING_PAGE_TITLE`|ランディングページのタイトル。メタデータの`LANDING_PAGE_TITLE`値は検索エンジンの結果に使用され、見出し1の`LANDING_PAGE_TITLE`値はページに表示されるタイトルに使用されます。|
| `SHORT_DESCRIPTION` | ページの1~2文の短い説明。YAMLにおけるメタデータの`SHORT_DESCRIPTION`値は検索エンジンの結果に使用され、見出し1以降の`SHORT_DESCRIPTION`値はページに表示される説明に使用されます。|
|`HEADING`|見出し2セクションのタイトル。|
|`CONTENT`|見出し2セクションの本文段落。|
{: .reset-td-br-1 .reset-td-br-2}

{% alert tip %}
このテンプレートは使い始めるためのものです。必要に応じて[メタデータ]({{site.baseurl}}/contributing/yaml_front_matter/metadata/)と見出しを追加してください。
{% endalert %}
{% endtab %}

{% tab without landing page %}
サブセクションのMarkdownファイルを開き、次のメタデータを追加してページのナビゲーションタイトルを設定し、ランディングページを無効にします。

\`\`マークダウン
---
nav_title: NAV\_TITLE
config_only: 真
---
\`\`\`

{% alert tip %}
このテンプレートは使い始めるためのものです。必要に応じて[メタデータ]({{site.baseurl}}/contributing/yaml_front_matter/metadata/)と見出しを追加してください。
{% endalert %}

`NAV_TITLE`は左側のナビゲーションバーに表示されるページのタイトルに置き換えてください。ページは次のようになります。

\`\`マークダウン
---
nav_title: はじめに
04
noindex: 真
config_only: 真
---
\`\`\`
{% endtab %}
{% endtabs %}

### ステップ 3ページを追加する

新しいディレクトリに、ページごとにMarkdownファイルを作成します。デフォルトのページレイアウトを使用するには、[手順2]({{site.baseurl}}/contributing/content_management/sections/?tab=with%20landing%20page#step-2-configure-your-section)のテンプレートを使用します。ディレクトリ構造は次のようになります。

```plaintext
braze-docs
└── _docs
    └── _developer_guide 
        └── platform_wide 
            ├── getting_started 
            │    ├── integrating_the_sdk.md 
            │    └── setting_up_push_notifications.md
            └── getting_started.md
```

各ページにコンテンツを追加し終えたら、[セクションの注文](#ordering-a-section)に進みます。

{% alert tip %}
ページにコンテンツを追加する手順の詳細については、「[ページ]({{site.baseurl}}/contributing/content_management/pages/#writing-content)」を参照してください。
{% endalert %}

## セクションの順序付け

セクションを注文するには、そのセクション内のMarkdownファイルのいずれかを開き、そのYAMLフロントマター内[で`page_order`]({{site.baseurl}}/contributing/yaml_front_matter/metadata/#page-order)キーを検索します。

\`\`マークダウン
---
page_order:
---
\`\`\`

`page_order`キーは、左側のナビゲーションバーのセクションにおけるページの相対順序を表し、負以外の任意の数値（`0`、`20`、`5.5`など）に設定できます。つまり、現在のディレクトリ内の各Markdownファイルの`page_order`は知る必要があるが、他のディレクトリ（サブディレクトリを含む）は知る必要がない。

カレントディレクトリ内の各Markdownファイルの`page_order`キーを負でない任意の数値に設定する。次の例では、`page_order`は`2`に設定されています。  

\`\`マークダウン
---
nav_title: B款
04 
---

# サブセクションBランディングページ
\`\`\`

出力は次のようになります。

![The left-side navigation on Braze Docs, with the 'Section B' landing page listed third.]({% image_buster /assets/img/contributing/styling_examples/subsection_landing_page.png %})
