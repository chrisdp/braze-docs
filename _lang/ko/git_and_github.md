---
nav_title: 깃과 깃허브
article: Git and GitHub
description: "Braze 문서에 기여할 수 있도록 Git과 GitHub를 사용하는 방법을 알아보세요."
page_order: 6
noindex: true
---

# 깃과 깃허브

> Braze 문서에 기여할 수 있도록 Git과 GitHub를 사용하는 방법을 알아보세요.

{% alert tip %}
Git이나 커맨드 라인을 처음 사용하는 경우 대신 튜토리얼부터 시작하세요. [귀하의 첫 번째 기여]({{site.baseurl}}/contributing/your_first_contribution/).
{% endalert %}

{% multi_lang_include contributing/prerequisites.md %}

## 브랜치 생성

새 Git 브랜치를 만들려면 먼저 브랜치를 체크아웃하고 로컬 환경을 업데이트하세요. `develop`

```bash
git checkout develop
git pull
```

Git 명령을 사용하여 새 Git 브랜치를 생성합니다. `checkout` 

```bash
git checkout -b BRANCH_NAME
```

브랜치 변경 사항을 `BRANCH_NAME` 공백으로 구분하지 않은 짧은 설명으로 대체하세요. 출력은 다음과 비슷해야 합니다.

```bash
$ git checkout -b fixing-typo-in-metadata
Switched to a new branch 'fixing-typo-in-metadata'
```

## 풀 리퀘스트 생성

풀 리퀘스트 (PR) 를 생성하려면 먼저 브랜치를 체크아웃하세요. 

```bash
git checkout BRANCH_NAME
```

[이전에 생성한](#creating-a-branch) 브랜치 `BRANCH_NAME` 이름으로 바꾸세요. 출력은 다음과 비슷해야 합니다.

```bash
$ git checkout fixing-typo-in-metadata
Switched to branch 'fixing-typo-in-metadata'
```

변경 사항을 추가하고 커밋을 스테이징하세요.

```bash
git add --all
git commit -m "COMMIT_MESSAGE"
```

변경 사항을 설명하는 짧은 문장으로 `COMMIT_MESSAGE` 바꾸세요. 출력은 다음과 비슷해야 합니다.

```bash
$ git commit -m "Fixing a typo in the recommended software doc
[fixing-typo-in-recommended-software 8b05e34] Fixing a typo in the metadata doc.
 1 file changed, 1 insertion(+), 1 deletion(-)
```

마지막으로 변경 사항을 Braze Docs GitHub 리포지토리로 푸시하세요.

```bash
git push -u origin BRANCH_NAME
```

지점 `BRANCH_NAME` 이름으로 바꾸십시오. 출력은 다음과 비슷합니다.

```bash
$ git push -u origin fixing-typo-in-recommended-software
Enumerating objects: 14, done.
...
To github.com:braze-inc/braze-docs.git
 * [new branch]      fixing-typo-in-recommended-software -> fixing-typo-in-recommended-software
branch 'fixing-typo-in-recommended-software' set up to track 'origin/fixing-typo-in-recommended-software'.
```

다음으로 [Braze Docs GitHub 리포지토리로](https://github.com/braze-inc/braze-docs) 이동한 다음 **비교** 및 풀 요청을 선택합니다.

![The Braze Docs GitHub repository showing "Open pull request".]({% image_buster /assets/img/contributing/github/compare_and_pull_request.png %})

PR 설명에서 다음과 비슷한 마크다운 댓글을 볼 수 있습니다. 이 댓글은 PR을 작성하는 데 도움이 됩니다.

\`\`\`마크다운
<!-- This is a Markdown comment. -->
```

완료하면 풀 리퀘스트 드롭다운을 선택한 다음 **초안 풀 리퀘스트를** 선택합니다.

![The Braze Docs GitHub repository showing "Draft pull request".]({% image_buster /assets/img/contributing/github/draft_pull_request.png %}){: style="max-width:65%;"}

## 리뷰 요청

Braze Docs 팀원에게 PR 검토를 [요청하려면 이전에 만든 PR을](#creating-a-pull-request) 열고 검토 **준비를** 선택합니다.

![An example pull request with the "Ready for review" button highlighted.]({% image_buster /assets/img/contributing/github/ready_for_review.png %}){: style="max-width:75%;"}

**리뷰어** 및 유형 `braze-inc/docs-team` 팀 이름을 선택하고 <kbd>Esc</kbd> 키를 누르거나 드롭다운을 클릭하여 선택을 확인합니다.

![An example pull request with "docs-team" added as the reviewer.]({% image_buster /assets/img/contributing/github/add_docs_team_as_reviewers.png %}){: style="max-width:55%;"}

Braze Docs 팀이 검토 후 추가 변경을 요청하면 [GitHub](https://docs.github.com/en/account-and-profile/managing-subscriptions-and-notifications-on-github/setting-up-notifications/configuring-notifications) 알림 설정에 따라 알림을 받게 됩니다. 변경이 필요하지 않은 경우 팀에서 변경 사항을 승인하고 병합합니다.

승인된 기부금은 다음 화요일 또는 목요일에 배포됩니다. 열심히 일한 것을 축하할 수 있도록 Braze Docs를 꼭 확인하세요. 기여해 주셔서 감사합니다!
