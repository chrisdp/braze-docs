---
nav_title: 집
article: Contributing to Braze Docs
description: "Braze Docs에 기여하기 위해 필요한 사항은 다음과 같습니다!"
page_order: 0
search_tag: Contributing
---

# Braze Docs에 기여

> Braze Docs에 기여해 주셔서 감사합니다! 매주 화요일과 목요일에는 커뮤니티 기여를 병합하여 Braze Docs에 배포합니다. 다음 배포 중에 변경 사항을 병합하려면 이 가이드를 사용하세요.

## 전제조건

Braze Docs에 기여하려면 Git에 대한 어느 정도의 이해가 필요합니다. Git을 처음 접하고 어디서부터 시작해야 할지 모르겠다면 다음을 참조하세요. [힘내 책: 시작하기](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control). 복습이 필요한 경우[Git 및 GitHub를]({{site.baseurl}}/contributing/git_and_github/)참조하세요.

## 1 단계: CLA에 서명하세요

Braze Docs에 기여하는 모든 사람은[기여 라이센스 계약(CLA)에](https://www.braze.com/docs/cla)서명해야 합니다. CLA에 서명하지 않으면 `@cla-bot`GitHub에서는 풀 요청을 자동으로 차단합니다.

## 2 단계: 환경 설정

Braze Docs에 복잡하거나 여러 페이지를 변경하려면 먼저 로컬 환경을 설정해야 합니다. 그러나 작은 단일 문서 변경은[GitHub에서 직접]({{site.baseurl}}/contributing/your_first_contribution/?tab=github#step-2-make-a-change)완료할 수 있습니다.

### 2.1단계: 필요한 소프트웨어 받기

최소한 터미널, 텍스트 편집기, Ruby 버전 관리자가 필요합니다. 어디서부터 시작해야 할지 모르겠다면 다음을 참조하세요.

<style>
table td {
    word-break: break-word;
}
</style>
<table>
<thead>
    <tr>
        <th>유형</th>
        <th>제품</th>
        <th>설명</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td>힘내 GUI</td>
        <td><a href="https://desktop.github.com/">GitHub 데스크탑</a></td>
        <td>터미널에 명령을 입력하는 대신 Git 명령을 실행하는 데 사용할 수 있는 그래픽 사용자 인터페이스(GUI)입니다.</td>
    </tr>    
    <tr>
        <td>단말기</td>
        <td><a href="https://wezfurlong.org/wezterm/index.html">Wezterm</a></td>
        <td>명령줄에서 명령을 실행하고 Braze Docs 저장소와 상호 작용할 수 있는 터미널 에뮬레이터입니다. Windows 운영 체제를 사용하는 경우 WSL(Linux용 Windows 하위 시스템)도 설치해야 합니다.</td>
    </tr>
    <tr>
        <td>터미널 확장</td>
        <td><a href="https://learn.microsoft.com/en-us/windows/wsl/install">Linux용 Windows 하위 시스템(WSL)*</a></td>
        <td>WSL을 사용하면 Linux 하위 시스템을 설치하고 Windows 운영 체제에서 Unix와 유사한 명령을 실행할 수 있습니다. Windows 운영 체제에서 기여하는 경우 문서에 언급된 모든 Unix 계열 명령을 사용할 수 있도록 WSL을 설치하는 것이 좋습니다.<br><br><em>* Windows에서만 사용할 수 있습니다.</em></td>
    </tr>
    <tr>
        <td>패키지 관리자</td>
        <td><a href="https://brew.sh/">홈브류</a></td>
        <td>Braze Docs에 기여하는 데 사용되는 다양한 명령줄 인터페이스(CLI) 도구를 설치하고 관리할 수 있는 패키지 관리자입니다.</td>
    </tr>
    <tr>
        <td>루비 버전 관리자</td>
        <td><a href="https://github.com/rbenv/rbenv#using-package-managers">rbenv</a></td>
        <td>로컬 환경을 설정할 때 Braze Docs에 필요한 Ruby 버전을 설치하고 관리할 수 있는 Ruby 버전 관리자입니다. 다른 Ruby 버전 관리자를 사용하려면<a href="https://www.ruby-lang.org/en/documentation/installation/#managers">Ruby의 지원되는 버전 관리자를</a>참조하세요.</td>
    </tr>
    <tr>
        <td>텍스트 에디터</td>
        <td><a href="https://code.visualstudio.com/download">비주얼 스튜디오 코드(VS Code)</a></td>
        <td>Braze Docs 저장소의 모든 파일을 편집할 수 있는 Microsoft의 모든 기능을 갖춘 텍스트 편집기입니다. 경험을 향상하려면 다음 플러그인을 설치하십시오.
            <ul>
                <li><a href="https://marketplace.visualstudio.com/items?itemName=sissel.shopify-liquid">액체 + 지킬 린터</a></li>
                <li><a href="https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint">마크다운 린터</a></li>
                <li><a href="https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker">맞춤법 검사기</a></li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>텍스트 에디터</td>
        <td><a href="https://www.jetbrains.com/idea/download/">Intellij의 IDEA 커뮤니티 에디션</a></td>
        <td>Braze Docs 저장소의 모든 파일을 편집할 수 있는 Intellij의 모든 기능을 갖춘 텍스트 편집기입니다. 경험을 향상하려면 다음 플러그인을 설치하십시오.
            <ul>
                <li><a href="https://plugins.jetbrains.com/plugin/7793-markdown">마크다운 린터</a></li>
                <li><a href="https://plugins.jetbrains.com/plugin/12175-grazie-lite">맞춤법 검사기</a></li>
            </ul>
        </td>
    </tr>
</tbody>
</table>
{: .reset-td-br-1 .reset-td-br-2}

{% alert note %}
글을 쓰는 시점에서 모든 소프트웨어는 무료입니다. 제품이 더 이상 무료가 아닌 경우[알려주시기 바랍니다](https://github.com/braze-inc/braze-docs/issues/new?assignees=&labels=issue&projects=&template=report_an_issue.md&title=).
{% endalert %}

### 2.2단계: GitHub 계정 설정

다음으로[GitHub 계정을 만들고](https://github.com/join) [SSH 키를 설정하세요](https://docs.github.com/en/enterprise-cloud@latest/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

{% alert note %}
[WSL을](https://learn.microsoft.com/en-us/windows/wsl/install)사용하는 경우 Linux 지침에 따라 SSH 키를 설정하세요.
{% endalert %}

### 2.3단계: 저장소 포크

[Braze Docs GitHub 저장소를](https://github.com/braze-inc/braze-docs)열고**Fork를**선택합니다.

![The Braze Docs GitHub repository showing "Fork".]({% image_buster /assets/img/contributing/github/fork_the_repository.png %})

{% alert tip %}
자세한 내용은 다음을 참조하세요. [GitHub: 포크에 대하여](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/about-forks).
{% endalert %}

기본 설정을 유지한 다음**포크 만들기 를**선택합니다.

![The Braze Docs GitHub repository showing "Create fork".]({% image_buster /assets/img/contributing/github/create_a_new_fork.png %})

포크된 저장소에서**코드**>**SSH**>를 선택합니다. <i class="fa-regular fa-clone"></i> **복사**.

![An example forked repository with the "Code" dropdown open showing the "Copy" option.]({% image_buster /assets/img/contributing/github/clone_the_fork.png %}){: style="max-width:50%;"}

터미널에서 홈 디렉터리를 연 다음 Braze Docs 저장소를 복제하세요.

```bash
cd ~
git clone git@github.com:braze-inc/braze-docs.git
```

### 2.4단계: 루비 설치

[로컬 사이트 미리보기를 생성]({{site.baseurl}}/contributing/generating_a_preview/)하려면 Ruby 버전이 필요합니다. `3.2.2`설치되었습니다. 터미널에서 다음을 엽니다. `braze-docs`Ruby 버전을 확인하세요. `3.2.2`.

```bash
cd ~/braze-docs
ruby --version
```

이 버전이 설치되어 있지 않으면[지원되는 버전 관리자를](https://www.ruby-lang.org/en/documentation/installation/#managers)사용하여 Ruby 버전을 설치하세요. `3.2.2`. 예를 들어[rbenv 를](https://github.com/rbenv/rbenv)사용합니다.

```bash
rbenv install 3.2.2
```

### 2.5단계: 종속성 설치

다음으로 Braze Docs에 대한 종속성을 설치합니다. 이는 로컬 Braze Docs 사이트를 생성하는 데 사용되는 작은 프로그램입니다.

```bash
bundle install
```

## 다음 단계

Git 또는 docs-as-code를 처음 사용하는 경우 튜토리얼부터 시작하세요. [귀하의 첫 번째 기여입니다]({{site.baseurl}}/contributing/your_first_contribution/). 그렇지 않은 경우 다음 중 하나를 확인하세요.

- [콘텐츠 관리]({{site.baseurl}}/contributing/content_management/)
- [YAML 메타데이터]({{site.baseurl}}/contributing/yaml_front_matter/metadata/)
- [미리보기 생성]({{site.baseurl}}/contributing/generating_a_preview/)
- [스타일 가이드]({{site.baseurl}}/contributing/style_guide)
