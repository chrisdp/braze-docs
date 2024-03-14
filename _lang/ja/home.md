---
nav_title: 家
article: Contributing to Braze Docs
description: "Braze Docs への貢献を始めるために必要なものは次のとおりです。"
page_order: 0
search_tag: Contributing
---

# Braze ドキュメントへの貢献

> Braze Docs にご協力いただきありがとうございます。毎週火曜日と木曜日に、コミュニティの投稿を統合して Braze Docs に展開します。このガイドを使用して、次回のデプロイ時に変更をマージします。

## 前提条件

Braze Docs に貢献するには、Git についてある程度の理解が必要です。Git を初めて使用するため、どこから始めればよいかわからない場合は、次を参照してください。 [Git ブック:はじめる](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)。復習が必要な場合は、[Git および GitHub]({{site.baseurl}}/contributing/git_and_github/)を参照してください。

## ステップ 3CLAに署名する

Braze Docs に貢献する人は全員、 [貢献ライセンス契約 (CLA)](https://www.braze.com/docs/cla)に署名する必要があります。CLA に署名しない場合、 `@cla-bot`GitHub ではプル リクエストが自動的にブロックされます。

## ステップ 3環境をセットアップする

Braze Docs に複雑な変更や複数ページの変更を加える前に、ローカル環境をセットアップする必要があります。ただし、単一ドキュメントの小さな変更は [GitHub で直接]({{site.baseurl}}/contributing/your_first_contribution/?tab=github#step-2-make-a-change)完了できます。

### ステップ 3必要なソフトウェアを入手する

少なくとも、ターミナル、テキスト エディタ、および Ruby バージョン マネージャーが必要です。どこから始めればよいかわからない場合は、以下を参照してください。

<style>
table td {
    word-break: break-word;
}
</style>
<table>
<thead>
    <tr>
        <th>タイプ</th>
        <th>製品</th>
        <th>説明</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td>Git GUI</td>
        <td><a href="https://desktop.github.com/">GitHub デスクトップ</a></td>
        <td>ターミナルにコマンドを入力する代わりに、Git コマンドを実行するために使用できるグラフィカル ユーザー インターフェイス (GUI)。</td>
    </tr>    
    <tr>
        <td>ターミナル</td>
        <td><a href="https://wezfurlong.org/wezterm/index.html">ウェスターム</a></td>
        <td>コマンドを実行し、コマンドラインから Braze Docs リポジトリと対話できるようにするターミナル エミュレーター。Windows オペレーティング システムを使用している場合は、Windows Subsystem for Linux (WSL) もインストールする必要があります。</td>
    </tr>
    <tr>
        <td>端子延長</td>
        <td><a href="https://learn.microsoft.com/en-us/windows/wsl/install">Linux 用 Windows サブシステム (WSL)*</a></td>
        <td>WSL を使用すると、Linux サブシステムをインストールし、Windows オペレーティング システム上で Unix のようなコマンドを実行できます。Windows オペレーティング システムから貢献している場合は、ドキュメントに記載されている Unix 風のコマンドを使用できるように、WSL をインストールすることをお勧めします。<br><br><em>※Windowsのみ利用可能です。</em></td>
    </tr>
    <tr>
        <td>パッケージマネージャー</td>
        <td><a href="https://brew.sh/">自作</a></td>
        <td>Braze Docs に貢献するために使用されるさまざまなコマンドライン インターフェイス (CLI) ツールのインストールと管理を可能にするパッケージ マネージャー。</td>
    </tr>
    <tr>
        <td>Rubyのバージョンマネージャー</td>
        <td><a href="https://github.com/rbenv/rbenv#using-package-managers">rbenv</a></td>
        <td>Ruby バージョン マネージャー。ローカル環境のセットアップ時に Braze Docs に必要な Ruby バージョンをインストールして管理できるようにします。別の Ruby バージョン マネージャーを使用する場合は、<a href="https://www.ruby-lang.org/en/documentation/installation/#managers">「Ruby でサポートされているバージョン マネージャー」</a>を参照してください。</td>
    </tr>
    <tr>
        <td>テキストエディタ</td>
        <td><a href="https://code.visualstudio.com/download">Visual Studio コード (VS コード)</a></td>
        <td>Braze Docs リポジトリ内の任意のファイルを編集できる Microsoft のフル機能のテキスト エディタです。エクスペリエンスを向上させるために、次のプラグインを必ずインストールしてください。
            <ul>
                <li><a href="https://marketplace.visualstudio.com/items?itemName=sissel.shopify-liquid">リキッド + ジキル リンター</a></li>
                <li><a href="https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint">マークダウンリンター</a></li>
                <li><a href="https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker">スペルチェッカー</a></li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>テキストエディタ</td>
        <td><a href="https://www.jetbrains.com/idea/download/">Intellij の IDEA コミュニティ エディション</a></td>
        <td>Intellij によるフル機能のテキスト エディター。Braze Docs リポジトリ内の任意のファイルを編集できます。エクスペリエンスを向上させるために、次のプラグインを必ずインストールしてください。
            <ul>
                <li><a href="https://plugins.jetbrains.com/plugin/7793-markdown">マークダウンリンター</a></li>
                <li><a href="https://plugins.jetbrains.com/plugin/12175-grazie-lite">スペルチェッカー</a></li>
            </ul>
        </td>
    </tr>
</tbody>
</table>
{: .reset-td-br-1 .reset-td-br-2}

{% alert note %}
執筆時点では、すべてのソフトウェアは無料です。製品が無料ではなくなった場合は、 [お知らせください](https://github.com/braze-inc/braze-docs/issues/new?assignees=&labels=issue&projects=&template=report_an_issue.md&title=)。
{% endalert %}

### ステップ 3GitHub アカウントをセットアップする

次に、[GitHub アカウントを作成し](https://github.com/join) 、[SSH キーを設定します](https://docs.github.com/en/enterprise-cloud@latest/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)。

{% alert note %}
[WSL](https://learn.microsoft.com/en-us/windows/wsl/install)を使用している場合は、Linux の手順に従って SSH キーを設定します。
{% endalert %}

### ステップ 3リポジトリをフォークする

[Braze Docs GitHub リポジトリ](https://github.com/braze-inc/braze-docs)を開き、**[フォーク]**を選択します。

![The Braze Docs GitHub repository showing "Fork".]({% image_buster /assets/img/contributing/github/fork_the_repository.png %})

{% alert tip %}
詳細については、「」を参照してください。 [GitHub:フォークについて](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/about-forks)。
{% endalert %}

デフォルト設定をそのままにして、**「フォークの作成」**を選択します。

![The Braze Docs GitHub repository showing "Create fork".]({% image_buster /assets/img/contributing/github/create_a_new_fork.png %})

フォークされたリポジトリで、**「コード」**>**「SSH」**> を選択します。 <i class="fa-regular fa-clone"></i>**コピー**。

![An example forked repository with the "Code" dropdown open showing the "Copy" option.]({% image_buster /assets/img/contributing/github/clone_the_fork.png %}){: style="max-width:50%;"}

ターミナルでホーム ディレクトリを開き、Braze Docs リポジトリのクローンを作成します。

```bash
cd ~
git clone git@github.com:braze-inc/braze-docs.git
```

### ステップ 3Rubyをインストールする

[ローカル サイトのプレビューを生成する]({{site.baseurl}}/contributing/generating_a_preview/)には、Ruby バージョンが必要です `3.2.2` インストールされています。ターミナルで開きます `braze-docs` Rubyのバージョンを確認してください `3.2.2`。

```bash
cd ~/braze-docs
ruby --version
```

このバージョンがインストールされていない場合は、 [サポートされているバージョン マネージャー](https://www.ruby-lang.org/en/documentation/installation/#managers) を使用して Ruby バージョンをインストールします `3.2.2`。たとえば、[rbenv を](https://github.com/rbenv/rbenv)使用します。

```bash
rbenv install 3.2.2
```

### ステップ 3依存関係をインストールする

次に、Braze Docs の依存関係をインストールします。これらは、ローカル Braze Docs サイトを生成するために使用される小さなプログラムです。

```bash
bundle install
```

## 次のステップ

Git や docs-as-code を初めて使用する場合は、チュートリアルから始めてください。[あなたの最初の貢献]({{site.baseurl}}/contributing/your_first_contribution/)。それ以外の場合は、次のいずれかを確認してください。

- [コンテンツ管理]({{site.baseurl}}/contributing/content_management/)
- [YAMLメタデータ]({{site.baseurl}}/contributing/yaml_front_matter/metadata/)
- [プレビューの生成]({{site.baseurl}}/contributing/generating_a_preview/)
- [スタイルガイド]({{site.baseurl}}/contributing/style_guide)
