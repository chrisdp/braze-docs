---
nav_title: Git と GitHub
article: Git and GitHub
description: "Git と GitHub の使用方法を学び、Braze Docs に貢献できるようにします。"
page_order: 6
noindex: true
---

# Git と GitHub

> Git と GitHub の使用方法を学び、Braze Docs に貢献できるようにします。

{% alert tip %}
Git やコマンドラインを初めて使用する場合は、代わりにチュートリアルから始めてください。[あなたの最初の貢献]({{site.baseurl}}/contributing/your_first_contribution/)。
{% endalert %}

{% multi_lang_include contributing/prerequisites.md %}

## ブランチの作成

新しい Git ブランチを作成するには、まず、 `develop` ブランチしてローカル環境を更新します。

```bash
git checkout develop
git pull
```

Git を使用して新しい Git ブランチを作成する `checkout` 指示。 

```bash
git checkout -b BRANCH_NAME
```

交換する `BRANCH_NAME` ブランチの変更内容をスペースで区切らずに短い説明で記述します。出力は次のようになります。

```bash
$ git checkout -b fixing-typo-in-metadata
Switched to a new branch 'fixing-typo-in-metadata'
```

## プルリクエストの作成

プル リクエスト (PR) を作成するには、まずブランチをチェックアウトします。 

```bash
git checkout BRANCH_NAME
```

交換する `BRANCH_NAME`[前に作成した](#creating-a-branch)ブランチの名前を付けます。出力は次のようになります。

```bash
$ git checkout fixing-typo-in-metadata
Switched to branch 'fixing-typo-in-metadata'
```

変更を追加し、コミットをステージングします。

```bash
git add --all
git commit -m "COMMIT_MESSAGE"
```

交換する `COMMIT_MESSAGE` 変更内容を説明する短い文を付けます。出力は次のようになります。

```bash
$ git commit -m "Fixing a typo in the recommended software doc
[fixing-typo-in-recommended-software 8b05e34] Fixing a typo in the metadata doc.
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

次に、[Braze Docs GitHub リポジトリ](https://github.com/braze-inc/braze-docs)に移動し、**[比較とプル リクエスト]**を選択します。

![The Braze Docs GitHub repository showing "Open pull request".]({% image_buster /assets/img/contributing/github/compare_and_pull_request.png %})

PR の説明には、次のようなマークダウン コメントが表示されます。これらのコメントを自己PRの記入に役立ててください。

\`\`\`マークダウン
<!-- This is a Markdown comment. -->
```

完了したら、プル リクエストのドロップダウンを選択し、**[ドラフト プル リクエスト]**を選択します。

![The Braze Docs GitHub repository showing "Draft pull request".]({% image_buster /assets/img/contributing/github/draft_pull_request.png %}){: style="max-width:65%;"}

## レビューのリクエスト

Braze Docs チームのメンバーに PR レビューをリクエストするには、 [以前に作成した PR を](#creating-a-pull-request) 開き、**[レビューの準備完了]**を選択します。

![An example pull request with the "Ready for review" button highlighted.]({% image_buster /assets/img/contributing/github/ready_for_review.png %}){: style="max-width:75%;"}

**査読者** とタイプ `braze-inc/docs-team`。チーム名を選択し、<kbd>Esc キー</kbd> を押すか、ドロップダウンをクリックして選択を確定します。

![An example pull request with "docs-team" added as the reviewer.]({% image_buster /assets/img/contributing/github/add_docs_team_as_reviewers.png %}){: style="max-width:55%;"}

Braze Docs チームがレビュー後に追加の変更をリクエストした場合は、[GitHub の通知設定](https://docs.github.com/en/account-and-profile/managing-subscriptions-and-notifications-on-github/setting-up-notifications/configuring-notifications)に従って通知されます。変更が必要ない場合は、チームが変更を承認してマージします。

承認されたコントリビューションは、次の火曜日または木曜日に展開されます。あなたの努力を称えるために、必ず Braze Docs をチェックしてください。貢献してくれてありがとう！
