---
nav_title: 첫 번째 기여
article: Your first contribution
description: "코드형 문서 또는 Braze Docs를 처음 사용하는 경우 이 단계별 자습서부터 시작하세요."
page_order: 1
noindex: true
---

# 첫 번째 기여

> 코드형 문서 또는 Braze Docs를 처음 사용하는 경우 이 단계별 자습서부터 시작하세요. 숙련된 기여자라면 대신 [콘텐츠 관리를]({{site.baseurl}}/contributing/content_management/) 참조하세요.

이 튜토리얼을 마치면 다음과 같이 할 수 있습니다:

- Braze Docs 깃허브 리포지토리 탐색하기
- GitHub 웹사이트 또는 로컬 환경을 사용하여 변경하기
- 풀 리퀘스트(PR) 만들기
- 테스트 사이트에서 변경 사항 미리보기
- 브레이즈 문서 팀에 검토 요청하기

{% multi_lang_include contributing/prerequisites.md %}

## 1단계: GitHub 리포지토리 살펴보기

Braze Docs [GitHub 리포지토리에는](https://github.com/braze-inc/braze-docs) Braze Docs의 소스 파일이 호스팅됩니다. 아직 모든 것을 이해하지 못하더라도 몇 분 정도 시간을 내어 리포지토리를 살펴보세요. 시간이 지나면 더 익숙해질 것입니다.

![The Braze Docs GitHub repository homepage.]({% image_buster /assets/img/contributing/github/home_page.png %})

## 2단계: 변경하기

이제 문서 리포지토리에 조금 익숙해졌으니 이제 변경을 시작할 준비가 되었습니다. 먼저 [Braze 문서를]({{site.baseurl}}) 열고 변경하고 싶은 간단한 사항을 찾은 다음, 어떻게 변경할지 결정합니다:

- **GitHub 사용(간편):** 소규모의 단일 문서 변경의 경우 GitHub 웹사이트에서 직접 변경할 수 있습니다.
- **로컬 환경 사용(고급):** 복잡하거나 여러 문서가 변경된 경우에는 로컬 환경에서 변경해야 합니다. 이 방법을 권장합니다.

{% tabs %}
{% tab github %}
[Braze Docs GitHub 리포지토리에서](https://github.com/braze-inc/braze-docs) `_docs` 을 선택합니다.

![The Braze Docs GitHub repository homepage with the '_docs' folder highlighted in the file tree.]({% image_buster /assets/img/contributing/github/select_docs_directory.png %})

Braze Docs의 각 페이지의 URL은 리포지토리의 디렉토리 구조를 반영합니다. 페이지의 URL을 사용하여 `_docs` 디렉터리에서 해당 마크다운 파일을 찾습니다. 예를 들어 `braze.com/contributing/home` 에 대한 마크다운 파일은 `_docs` > `_contributing` > `home.md` 에서 찾을 수 있습니다.

![The home page for the "Contributing" section on Braze Docs.]({% image_buster /assets/img/contributing/github/example_file_path.png %})

**이 파일 편집을** 선택한 다음 [마크다운 서식을](https://www.markdownguide.org/basic-syntax/) 사용하여 변경합니다.

![An example page on Braze Docs showing "Edit this file".]({% image_buster /assets/img/contributing/github/edit_from_directory.png %})

완료했으면 **변경 사항 커밋을** 선택합니다.

![The Braze Docs GitHub repository showing "Commit changes" after editing a file.]({% image_buster /assets/img/contributing/github/commit_changes.png %})

다음 창에서 **변경 제안을** 선택합니다.

![The "Propose changes" window after selecting "Commit changes" in GitHub.]({% image_buster /assets/img/contributing/github/propose_changes.png %}){: style="max-width:65%;"}
{% endtab %}

{% tab local environment %}
{% alert important %}
계속하기 전에 모든 [필수](#prerequisites) 요건을 완료했는지 확인하세요.
{% endalert %}

대부분의 최신 텍스트 편집기(예: [VS Code](https://code.visualstudio.com/Download) 및 [Intellij IDEA](https://www.jetbrains.com/idea/download/))는 명령을 실행하고 프로젝트 파일과 상호 작용할 수 있는 인앱 터미널을 제공합니다. 텍스트 편집기를 연 다음 텍스트 편집기의 앱 내 터미널을 엽니다.

![Intellij IDEA with the in-app terminal open.]({% image_buster /assets/img/contributing/text_editor_with_terminal.png %})

{% alert tip %}
문제가 있는 경우 독립형 단말기를 대신 사용할 수 있습니다.
{% endalert %}

터미널에서 `braze-docs` 디렉터리를 엽니다.

```bash
cd ~/PATH_TO_REPOSITORY
```

`PATH_TO_REPOSITORY` 을 [환경 설정]({{site.baseurl}}/contributing/home/#step-2-set-up-your-environment) 시 `braze-docs` 리포지토리를 저장한 위치로 바꿉니다. 명령은 다음과 유사해야 합니다:

```bash
cd ~/braze/braze-docs
```

`braze-docs` 디렉터리에 있는지 확인한 다음 Git 상태를 확인합니다.

```bash
pwd
git status
```

{% alert tip %}
`git status` 는 Git 디렉터리의 현재 상태를 표시합니다. Git을 처음 사용하는 경우 모든 단계 후에 이 명령을 실행하여 Git 워크플로를 시각화할 수 있습니다. 자세한 내용은 [`git status`](https://git-scm.com/docs/git-status).
{% endalert %}

문서 리포지토리에서 `develop` 브랜치는 최신 버전의 Braze 문서를 반영합니다. `develop` 브랜치를 확인하여 최신 업데이트를 로컬 환경에 적용하세요.

```bash
git checkout develop
git pull
```

문서를 변경할 때는 항상 새 브랜치를 만듭니다. 새 브랜치를 만들려면 `-b` 플래그와 함께 `git branch` 을 사용합니다.

```bash
git checkout -b BRANCH_NAME
```

`BRANCH_NAME` 을 공백으로 구분하지 않은 짧은 변경 내용 설명으로 바꿉니다. 명령은 다음과 유사해야 합니다:

```bash
$ git checkout -b fixing-typo-in-metadata
Switched to a new branch 'fixing-typo-in-metadata'
```

텍스트 편집기에서 변경하려는 문서를 연 다음, [마크다운 서식을](https://www.markdownguide.org/basic-syntax/) 사용하여 변경합니다.

{% multi_lang_include contributing/alerts/tip_locating_a_file.md %}

작업이 끝나면 변경 내용을 저장한 다음 터미널을 선택하고 Git 상태를 확인합니다. 출력은 다음과 비슷합니다:

\`\`\`bash
$ git status
메타데이터 내 브랜치 수정-오타에 대해
커밋을 위해 스테이징되지 않은 변경 사항입니다:
  (커밋할 내용을 업데이트하려면 "git add <file>..."를 사용하세요).
  (작업 디렉터리의 변경 사항을 삭제하려면 "git restore <file>..."를 사용하세요).
        수정되었습니다:   수정됨: \_docs/_home/metadata.md

커밋에 추가된 변경 사항이 없음("git add" 및/또는 "git commit -a" 사용)
\`\`\`

`git add` 을 사용하여 커밋을 위해 어떤 변경 사항을 스테이징할지 Git에 알려주세요. 다음 명령은 두 가지 옵션을 보여줍니다:

- **파이프의 왼쪽:** `--all` 을 사용하여 변경된 파일을 모두 추가합니다.
- **파이프의 오른쪽:** `PATH_TO_FILE` 을 변경한 파일의 상대 경로로 대체하여 개별 파일을 추가합니다.

```bash
git add {--all|PATH_TO_FILE}
```

`-m` 플래그와 함께 `git commit` 를 사용하여 간단한 설명(또는 메시지)과 함께 커밋을 생성하세요.

```bash
git commit -m "COMMIT_MESSAGE"
```

`COMMIT_MESSAGE` 을 변경 사항을 설명하는 짧은 문장으로 바꿉니다. 명령은 다음과 유사해야 합니다:

```bash
$ git commit -m "Fixing a typo in the recommended software doc"
[fixing-typo-in-recommended-software 8b05e34] Fixing a typo in the recommended software doc.
 1 file changed, 1 insertion(+), 1 deletion(-)
```

마지막으로, 변경 사항을 Braze Docs GitHub 리포지토리에 푸시합니다.

```bash
git push -u origin BRANCH_NAME
```

`BRANCH_NAME` 을 지사 이름으로 바꿉니다. 출력은 다음과 비슷합니다:

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

## 3단계: 풀 리퀘스트(PR) 만들기

아직 없는 경우 [리포지토리 홈페이지로](https://github.com/braze-inc/braze-docs) 돌아가서 **비교 및 풀리퀘스트를** 선택하세요.

![The Braze Docs GitHub repository homepage showing "Open pull request".]({% image_buster /assets/img/contributing/github/compare_and_pull_request.png %})

PR 설명에서 다음과 유사한 마크다운 댓글을 볼 수 있습니다:

'''마크다운
<!-- This is a Markdown comment. -->
```

이 댓글을 통해 PR 설명을 작성할 수 있습니다. 완료했으면 풀리퀘스트 드롭다운을 선택한 다음 **초안 풀리퀘스트를** 선택합니다.

![An example pull request showing "Draft pull request".]({% image_buster /assets/img/contributing/github/draft_pull_request.png %}){: style="max-width:65%;"}

## 4단계: 작업 검토

사이트 미리 보기에서 작업을 검토하여 콘텐츠가 [Braze Docs 스타일 가이드를]({{sitebase.url}}/contributing/style_guide/) 따르고 있는지 확인하세요. 추가 변경이 필요한 경우 [추가 변경하기를](#step-6-make-additional-changes-optional) 참조하세요. 그렇지 않은 경우 Braze 문서 팀에 [검토를 요청할](#step-5-request-a-review) 수 있습니다.

{% tabs %}
{% tab github %}
PR 댓글에 `@braze-inc/docs-team` 태그를 지정하여 사이트 미리 보기를 요청하세요.

![An example comment tagging the Braze Docs team to request a site preview.]({% image_buster /assets/img/contributing/github/tag_docs_team_in_comment.png %}){: style="max-width:83%;"}

사이트 미리 보기를 열려면 **배포 보기를** 선택합니다.

![An example pull request showing the "View deployment" button generated by the Vercel bot.]({% image_buster /assets/img/contributing/github/view_deployment.png %})

{% endtab %}

{% tab local environment %}
터미널에서 `rake` 명령을 사용하여 로컬 서버를 시작합니다.

```bash
cd ~/braze-docs
rake
```

출력은 다음과 비슷합니다:

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

기본적으로 사이트 미리 보기는 localhost [`http://127.0.0.1:4000`](http://127.0.0.1:4000). 사이트 미리 보기를 열려면 웹 브라우저에서 링크를 엽니다.

![An example site preview running in a web browser.]({% image_buster /assets/img/contributing/styling_examples/home.png %})

로컬 서버를 중지하려면 터미널을 다시 열고 <kbd>Control</kbd> + <kbd>C를</kbd> 누릅니다.

{% alert tip %}
전체 안내는 [미리 보기 생성을]({{site.baseurl}}/contributing/generating_a_preview/) 참조하세요.
{% endalert %}
{% endtab %}
{% endtabs %}

## 5단계: 검토 요청하기

Braze Docs 팀원이 작업을 검토할 준비가 되었다면 **검토 준비됨을** 선택하세요.

![An example pull request showing "Ready for review".]({% image_buster /assets/img/contributing/github/ready_for_review.png %}){: style="max-width:75%;"}

**검토자를** 입력하고 `braze-inc/docs-team` 을 입력합니다. 팀 이름을 선택하고 <kbd>Esc</kbd> 키를 누르거나 드롭다운에서 클릭하여 선택을 확인합니다.

![An example pull request with "docs-team" added as the reviewer.]({% image_buster /assets/img/contributing/github/add_docs_team_as_reviewers.png %}){: style="max-width:55%;"}

문서 팀이 검토 후 추가 변경을 요청하면 [GitHub 알림 설정에](https://docs.github.com/en/account-and-profile/managing-subscriptions-and-notifications-on-github/setting-up-notifications/configuring-notifications) 따라 알림을 받게 됩니다. 그렇지 않으면 문서 팀에서 변경 사항을 승인하고 병합합니다.

승인된 기여는 다음 주 화요일 또는 목요일에 배포됩니다. Braze Docs에서 여러분의 노력을 확인해보세요. 참여해 주셔서 감사합니다!

## 6단계: 추가 변경(선택 사항)

사용자 또는 Braze Docs 팀원이 작업을 검토한 후 PR을 추가로 변경해야 할 수도 있습니다. 로컬 환경 또는 GitHub를 사용하여 수행할 수 있습니다.

{% tabs %}
{% tab github %}
PR에서 **변경된 파일을** 선택한 다음 업데이트하려는 파일을 찾아 <i class="fa-solid fa-ellipsis"></i> **옵션 표시** > **파일 편집을** 선택합니다.

![The "Files changed" section in an example pull request showing "Edit file".]({% image_buster /assets/img/contributing/github/edit_from_pr.png %})

완료했으면 **변경 사항 커밋을** 선택합니다.

![A file from an example pull request showing "Commit changes" after editing.]({% image_buster /assets/img/contributing/github/commit_changes.png %})

**브랜치 이름 브랜치에 직접 커밋하기** > **변경 사항 커밋을** 선택합니다. 여기서 `BRANCH_NAME` 은 **브랜치** 이름입니다.

![The "Commit changes" option after choosing "Commit directly to BRANCH_NAME branch.]({% image_buster /assets/img/contributing/github/confirm_committed_changes.png %}){: style="max-width:65%;"}

완료되면 [검토를 요청하세요](#step-5-request-a-review).
{% endtab %}

{% tab local environment %}
PR에서 브랜치 이름 옆에 있는 <i class="fa-regular fa-clone"></i> **복사를** 선택합니다.

![An example pull request with the "Copy" icon shown next to the branch name.]({% image_buster /assets/img/contributing/github/clone_the_fork.png %})

텍스트 편집기의 터미널에서 브랜치를 체크아웃하고 GitHub의 원격 브랜치에서 최신 업데이트를 가져옵니다.

```bash
git checkout BRANCH_NAME && git pull
```

`BRANCH_NAME` 을 클립보드에 복사한 브랜치 이름으로 바꿉니다. 출력은 다음과 비슷합니다:

```bash
$ git checkout fixing-typo-in-metadata  && git pull
Switched to branch 'fixing-typo-in-metadata'
Your branch is up to date with 'origin/fixing-typo-in-metadata'.
```

텍스트 편집기에서 변경하려는 문서를 연 다음 [2단계에서 이전에 완료한 단계를 반복합니다: 변경하기](#step-2-make-a-change).
{% endtab %}
{% endtabs %}
