---
nav_title: コンテンツの再利用
article: Reusing content
description: "Braze Docs全体でコンテンツを再利用する方法を学ぶことで、コンテンツの一貫性を高め、コンテンツ作成の時間を短縮できる。"
page_order: 5
noindex: true
---

# コンテンツの再利用

> Braze Docs全体でコンテンツを再利用する方法を学ぶことで、コンテンツの一貫性を高め、コンテンツ作成の時間を短縮できる。コンテンツの再利用に関する一般的な情報は、[コンテンツ]({{site.baseurl}}/contributing/content_management/#content-reuse)管理を参照のこと。

Jekyllのコンテンツの再利用は、インクルードを使用して達成される。インクルードは通常のMarkdownファイルとして`_includes` ディレクトリに保存される。しかし、`_docs` ディレクトリのMarkdownファイルとは異なり、これらのファイルはYAMLのフロントマターを必要としない。

{% multi_lang_include contributing/prerequisites.md %}

## インクルードを作成する

`_includes` ディレクトリに、`.md` の拡張子を持つ新しいMarkdownファイルを作成する。インクルードファイルはこのディレクトリのどこにでも格納できるが、サブディレクトリを使って関連するコンテンツをまとめておくのがベストだ。ファイルツリーは以下のようになっているはずだ：

```bash
braze-docs
└── _includes
    ├── alerts
    ├── archive
    └── contributing
        └── site_generator.md
```

ページにコンテンツを追加し、[Braze Docsスタイルガイドに]({{site.baseurl}}/contributing/style_guide/)従うこと。すでにYAMLのフロントマターを持っているページにインクルードを追加するつもりなら、インクルードにフロントマターを追加しないこと。内容は以下のようなものであるべきだ：

{% raw %}
マークダウン
## サイト・ジェネレーター 

Braze Docsは、Jekyllを使用して構築されている。Jekyllは一般的な静的サイトジェネレーター（SSG）で、コンテンツファイルとデザインファイルを別々のディレクトリ（コンテンツファイルは`_docs` 、デザインファイルは`assets` ）に保存できる。サイトが構築されると、Jekyllはインテリジェントに各ファイルをマージし、XMLとHTMLデータとして`_site` ディレクトリに格納される。詳細については、参照してください[Jekyllディレクトリ構造](https://jekyllrb.com/docs/structure/).

![The home page for Braze Docs.]({% image_buster /assets/img/contributing/braze_docs_github.png %})

コントリビューターとして、主に以下のディレクトリを担当する。

| ディレクトリ
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`_docs`](https://github.com/braze-inc/braze-docs/tree/develop/_docs)         | Braze DocsのすべてのコンテンツがMarkdownで書かれたテキストファイルとして格納されている。テキストファイルは、[APIセクションは]({{site.baseurl}}/api/home) `_api` 、[ユーザーガイドセクションは]({{site.baseurl}}/user_guide/introduction) `user_guide` のように、docsサイトを反映したディレクトリとサブディレクトリに編成されている。|
| [`_includes`](https://github.com/braze-inc/braze-docs/tree/develop/_includes)|`_docs` ディレクトリ内のどのファイルでも再利用できるテキストファイル（「インクルード」と呼ばれる）を含む。通常、インクルードとは、標準的な書式を使用しない、短くてモジュール化されたコンテンツのことである。この場所に保存されているファイルは、[コンテンツの再利用にとって](#content-reuse)重要である。                                            |
| [`assets`](https://github.com/braze-inc/braze-docs/tree/develop/assets)       | Braze Docsの全画像を含む。`_docs` または`_includes` ディレクトリにあるテキストファイルは、このディレクトリにリンクして、そのページに画像を表示することができる。                                                                                                                                                                         |
{: .reset-td-br-1 .reset-td-br-2}
\`\`\`
{% endraw %}

{% alert tip %}
詳しい解説は、[コンテンツを書くを]({{site.baseurl}}/contributing/content_management/pages/#writing-content)参照のこと。
{% endalert %}

## インクルードを参照する

インクルードを参照するには、関連するMarkdownファイル内で以下の構文を使う：

{% raw %}
```plaintext
{% multi_lang_include PATH_TO_INCLUDE %}
```
{% endraw %}

`PATH_TO_INCLUDE` を`_includes` ディレクトリ内からの相対パスに置き換える。例えば、次のようなファイルツリーがあるとする：

```bash
braze-docs
└── _includes
    ├── alerts
    ├── archive
    └── contributing
        └── prerequisites.md
```

参考文献は以下のようなものだ：

{% tabs local %}
{% tab example input %}
{% raw %}
マークダウン
# ページ

> Braze Docsでページを作成、変更、削除する方法を学ぶ。

{% multi_lang_include contributing/prerequisites.md %}
\`\`\`
{% endraw %}
{% endtab %}

{% tab example output %}
![Content reuse example on Braze Docs.]({% image_buster /assets/img/contributing/styling_examples/includes.png %}){: style="max-width:90%;"}
{% endtab %}
{% endtabs %}
