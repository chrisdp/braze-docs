---
nav_title: 初めての貢献
article: Your first contribution
description: "docs-as-code または Braze Docs を初めて使用する場合は、このステップバイステップのチュートリアルから始めてください。"
page_order: 1
noindex: true
---

# あなたの最初の貢献

> docs-as-code または Braze Docs を初めて使用する場合は、このステップバイステップのチュートリアルから始めてください。経験豊富な寄稿者の方は、代わりに [「コンテンツ管理」]({{site.baseurl}}/contributing/content_management/) を参照してください。

このチュートリアルを完了すると、次のことができるようになります。

- Braze Docs GitHub リポジトリに移動する
- GitHub Web サイトまたはローカル環境を使用して変更を加える
- プル リクエスト (PR) を作成する
- テストサイトで変更をプレビューする
- Braze Docs チームにレビューをリクエストする

{% multi_lang_include contributing/prerequisites.md %}

## ステップ 3GitHub リポジトリを探索する

[Braze Docs GitHub リポジトリは、](https://github.com/braze-inc/braze-docs)Braze Docs のソース ファイルをホストします。まだすべてを理解していなくても、数分かけてリポジトリを探索してください。時間が経つにつれて、より親しみやすくなります。

![The Braze Docs GitHub repository homepage.]({% image_buster /assets/img/contributing/github/home_page.png %})

## ステップ 3変える

docs リポジトリについて少し理解できたので、変更を開始する準備が整いました。まず、[Braze Docs を]({{site.baseurl}}) 開いて、加えたい簡単な変更を見つけて、それをどのように行うかを決定します。

- **GitHub の使用 (シンプル):**単一ドキュメントの小規模な変更の場合は、GitHub Web サイトから直接変更を加えることができます。
- **ローカル環境の使用 (詳細):**複雑な変更や複数のドキュメントの変更の場合は、ローカル環境から変更を加える必要があります。これが推奨される方法です。

{% tabs %}
{% tab github %}
[Braze Docs GitHub リポジトリ](https://github.com/braze-inc/braze-docs)で、 `_docs`。

![The Braze Docs GitHub repository homepage with the '_docs' folder highlighted in the file tree.]({% image_buster /assets/img/contributing/github/select_docs_directory.png %})

Braze Docs の各ページの URL は、リポジトリのディレクトリ構造を反映しています。ページの URL を使用して、対応する Markdown ファイルを見つけます。 `_docs` ディレクトリ。たとえば、次の Markdown ファイル `braze.com/contributing/home` で見つけることができます `_docs` > `_contributing`> `home.md`。

![The home page for the "Contributing" section on Braze Docs.]({% image_buster /assets/img/contributing/github/example_file_path.png %})

**[このファイルを編集]**を選択し、 [マークダウン形式](https://www.markdownguide.org/basic-syntax/)を使用して変更を加えます。

![An example page on Braze Docs showing "Edit this file".]({% image_buster /assets/img/contributing/github/edit_from_directory.png %})

完了したら、**[変更をコミット]**を選択します。

![The Braze Docs GitHub repository showing "Commit changes" after editing a file.]({% image_buster /assets/img/contributing/github/commit_changes.png %})

次のウィンドウで、**[変更の提案]**を選択します。

![The "Propose changes" window after selecting "Commit changes" in GitHub.]({% image_buster /assets/img/contributing/github/propose_changes.png %}){: style="max-width:65%;"}
{% endtab %}

{% tab local environment %}
{% alert important %}
続行する前に、すべての [前提条件](#prerequisites)を満たしていることを確認してください。
{% endalert %}

最新のテキスト エディター ([VS Code](https://code.visualstudio.com/Download) や [Intellij IDEA](https://www.jetbrains.com/idea/download/)など) のほとんどは、コマンドを実行したり、プロジェクト ファイルを操作したりするためのアプリ内ターミナルを提供します。テキスト エディターを開き、テキスト エディターのアプリ内ターミナルを開きます。

![Intellij IDEA with the in-app terminal open.]({% image_buster /assets/img/contributing/text_editor_with_terminal.png %})

{% alert tip %}
問題がある場合は、代わりにスタンドアロン ターミナルを使用できます。
{% endalert %}

ターミナルで、 `braze-docs` ディレクトリ。

```bash
cd ~/PATH_TO_REPOSITORY
```

交換する `PATH_TO_REPOSITORY` 保存した場所に合わせて、 `braze-docs`[環境をセットアップする]({{site.baseurl}}/contributing/home/#step-2-set-up-your-environment)ときにリポジトリを作成します。コマンドは次のようになります。

```bash
cd ~/braze/braze-docs
```

にいるかどうかを確認してください `braze-docs` ディレクトリに移動し、Git のステータスを確認します。

```bash
pwd
git status
```

{% alert tip %}
`git status` Git ディレクトリの現在のステータスを表示します。Git を初めて使用する場合は、各ステップの後にこのコマンドを実行して、Git ワークフローを視覚化することができます。詳細については、「」を参照してください。 [`git status`](https://git-scm.com/docs/git-status)。
{% endalert %}

ドキュメント リポジトリでは、 `develop` ブランチには Braze Docs の最新バージョンが反映されています。をチェックしてください `develop` ブランチして、最新の更新をローカル環境にプルします。

```bash
git checkout develop
git pull
```

ドキュメントに変更を加える場合は、常に新しいブランチを作成します。使用 `git branch` 一緒に `-b` 新しいブランチを作成するフラグ。

```bash
git checkout -b BRANCH_NAME
```

交換する `BRANCH_NAME` 変更内容をスペースで区切らずに短い説明で記述します。コマンドは次のようになります。

```bash
$ git checkout -b fixing-typo-in-metadata
Switched to a new branch 'fixing-typo-in-metadata'
```

テキスト エディタで、変更するドキュメントを開き、 [マークダウン形式を](https://www.markdownguide.org/basic-syntax/)使用して変更を加えます。

{% multi_lang_include contributing/alerts/tip_locating_a_file.md %}

完了したら、変更を保存し、ターミナルを選択して Git のステータスを確認します。出力は次のようになります。

「」バッシュ
$ gitステータス
ブランチでのメタデータのタイプミスの修正
コミットのためにステージングされていない変更:
  (「git add」を使用します <file>..." コミットされる内容を更新します)
  (「git 復元」を使用します) <file>..." 作業ディレクトリ内の変更を破棄します)
        変更されました: \_docs/_home/metadata.md

コミットに変更は追加されません (「git add」および/または「git commit -a」を使用)
\`\`\`

使用 `git add` コミットのためにどの変更をステージングするかを Git に伝えます。次のコマンドは 2 つのオプションを示しています。

- **パイプの左側:**次を使用して、変更したすべてのファイルを追加します `--all`。
- **パイプの右側:**置き換えて個別のファイルを追加します `PATH_TO_FILE` 変更したファイルへの相対パスで置き換えます。

```bash
git add {--all|PATH_TO_FILE}
```

使用 `git commit` とともに `-m` フラグを使用して、短い説明 (またはメッセージ) とともにコミットを作成します。

```bash
git commit -m "COMMIT_MESSAGE"
```

交換する `COMMIT_MESSAGE` 変更内容を説明する短い文を付けます。コマンドは次のようになります。

```bash
$ git commit -m "Fixing a typo in the recommended software doc"
[fixing-typo-in-recommended-software 8b05e34] Fixing a typo in the recommended software doc.
 1 file changed, 1 insertion(+), 1 deletion(-)
```

最後に、変更を Braze Docs GitHub リポジトリにプッシュします。

```bash
git push -u origin BRANCH_NAME
```

交換する `BRANCH_NAME` 支店の名前を付けてください。出力は次のようになります。

```bash
$ git push -u origin fixing-typo-in-recommended-software
Enumerating objects: 14, done.
...
To github.com:braze-inc/braze-docs.git
 * [new branch]      fixing-typo-in-recommended-software -> fixing-typo-in-recommended-software
branch 'fixing-typo-in-recommended-software' set up to track 'origin/fixing-typo-in-recommended-software'.
```
{% endtab %}
{% endtabs %}

## ステップ 3プルリクエスト (PR) を作成する

まだ [リポジトリのホームページに戻っていない場合は、リポジトリのホームページ](https://github.com/braze-inc/braze-docs) に戻り、**[比較とプル リクエスト]**を選択します。

![The Braze Docs GitHub repository homepage showing "Open pull request".]({% image_buster /assets/img/contributing/github/compare_and_pull_request.png %})

PR の説明には、次のようなマークダウン コメントが表示されます。

\`\`\`マークダウン
<!-- This is a Markdown comment. -->
```

これらのコメントは、PR の説明のガイドとなります。完了したら、プル リクエストのドロップダウンを選択し、**[ドラフト プル リクエスト]**を選択します。

![An example pull request showing "Draft pull request".]({% image_buster /assets/img/contributing/github/draft_pull_request.png %}){: style="max-width:65%;"}

## ステップ 3自分の仕事を見直してください

サイトのプレビューで作品を確認して、コンテンツが [Braze Docs スタイル ガイド]({{sitebase.url}}/contributing/style_guide/) に従っていることを確認してください。追加の変更を行う必要がある場合は、[「追加の変更を行う」](#step-6-make-additional-changes-optional)を参照してください。それ以外の場合は、Braze Docs チームに [レビューをリクエスト](#step-5-request-a-review) できます。

{% tabs %}
{% tab github %}
PR コメントにタグを付けます `@braze-inc/docs-team` サイトのプレビューをリクエストします。

![An example comment tagging the Braze Docs team to request a site preview.]({% image_buster /assets/img/contributing/github/tag_docs_team_in_comment.png %}){: style="max-width:83%;"}

サイトのプレビューを開くには、**[展開の表示]**を選択します。

![An example pull request showing the "View deployment" button generated by the Vercel bot.]({% image_buster /assets/img/contributing/github/view_deployment.png %})

{% endtab %}

{% tab local environment %}
ターミナルで、 `rake` コマンドでローカルサーバーを起動します。

```bash
cd ~/braze-docs
rake
```

出力は次のようになります。

```bash
== Sinatra (v3.0.4) has taken the stage on 4000 for development with backup from Puma
Puma starting in single mode...
* Puma version: 6.3.1 (ruby 3.2.2-p225) ("Mugi No Toki Itaru")
*  Min threads: 8
*  Max threads: 32
*  Environment: development
*          PID: 16158
* Listening on http://127.0.0.1:4000
...
```

デフォルトでは、サイトのプレビューはローカルホスト上に生成されます [`http://127.0.0.1:4000`](http://127.0.0.1:4000)。サイトのプレビューを開くには、Web ブラウザーでリンクを開きます。

![An example site preview running in a web browser.]({% image_buster /assets/img/contributing/styling_examples/home.png %})

ローカルサーバーを停止するには、ターミナルを再度開き、<kbd>Control</kbd>+<kbd>C</kbd>を押します。

{% alert tip %}
完全なチュートリアルについては、[「プレビューの生成」]({{site.baseurl}}/contributing/generating_a_preview/)を参照してください。
{% endalert %}
{% endtab %}
{% endtabs %}

## ステップ 3レビューをリクエストする

Braze Docs チームのメンバーに自分の作業をレビューしてもらう準備ができている場合は、**[レビューの準備完了]**を選択します。

![An example pull request showing "Ready for review".]({% image_buster /assets/img/contributing/github/ready_for_review.png %}){: style="max-width:75%;"}

**査読者** とタイプ `braze-inc/docs-team`。チーム名を選択し、<kbd>Esc キー</kbd> を押すか、ドロップダウンをクリックして選択を確定します。

![An example pull request with "docs-team" added as the reviewer.]({% image_buster /assets/img/contributing/github/add_docs_team_as_reviewers.png %}){: style="max-width:55%;"}

ドキュメント チームがレビュー後に追加の変更をリクエストした場合は、[GitHub の通知設定](https://docs.github.com/en/account-and-profile/managing-subscriptions-and-notifications-on-github/setting-up-notifications/configuring-notifications)に従って通知されます。それ以外の場合は、ドキュメント チームが変更を承認してマージします。

承認されたコントリビューションは、次の火曜日または木曜日に展開されます。Braze Docs を必ずチェックして、あなたの努力を確認してください。貢献してくれてありがとう！

## ステップ 3追加の変更を加えます (オプション)

あなたまたは Braze Docs チームのメンバーがあなたの作品をレビューした後、PR に追加の変更を加える必要がある場合があります。これは、ローカル環境または GitHub を使用して行うことができます。

{% tabs %}
{% tab github %}
PR で [ **変更されたファイル]**を選択し、更新するファイルを見つけて選択します。 <i class="fa-solid fa-ellipsis"></i> **[オプションを表示]**>**[ファイルを編集]**。

![The "Files changed" section in an example pull request showing "Edit file".]({% image_buster /assets/img/contributing/github/edit_from_pr.png %})

完了したら、**[変更をコミット]**を選択します。

![A file from an example pull request showing "Commit changes" after editing.]({% image_buster /assets/img/contributing/github/commit_changes.png %})

**[BRANCH\_NAME ブランチに直接コミット]**>**[変更をコミット]**を選択します。 `BRANCH_NAME` は支店の名前です。

![The "Commit changes" option after choosing "Commit directly to BRANCH_NAME branch.]({% image_buster /assets/img/contributing/github/confirm_committed_changes.png %}){: style="max-width:65%;"}

完了したら、 [レビューをリクエストします](#step-5-request-a-review)。
{% endtab %}

{% tab local environment %}
PR で選択します <i class="fa-regular fa-clone"></i> ブランチ名の横に **コピーします** 。

![An example pull request with the "Copy" icon shown next to the branch name.]({% image_buster /assets/img/contributing/github/clone_the_fork.png %})

テキスト エディターのターミナルでブランチをチェックアウトし、GitHub のリモート ブランチから最新の更新を取得します。

```bash
git checkout BRANCH_NAME && git pull
```

交換する `BRANCH_NAME` クリップボードにコピーしたブランチ名を置き換えます。出力は次のようになります。

```bash
$ git checkout fixing-typo-in-metadata  && git pull
Switched to branch 'fixing-typo-in-metadata'
Your branch is up to date with 'origin/fixing-typo-in-metadata'.
```

テキスト エディタで、変更するドキュメントを開き、以前に完了した手順を繰り返します。 [ステップ2：変える](#step-2-make-a-change)。
{% endtab %}
{% endtabs %}
