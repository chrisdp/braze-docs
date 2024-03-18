---
nav_title: 미리보기 생성
article: Generating a preview
description: "로컬 사이트 미리보기를 생성하는 방법을 알아보고 Braze Docs에서 작업이 어떻게 보이는지 확인하세요."
page_order: 5 
noindex: true
---

# 미리보기 생성

> 로컬 사이트 미리보기를 생성하는 방법을 알아보고 Braze Docs에서 작업이 어떻게 보이는지 확인하세요.

{% multi_lang_include contributing/prerequisites.md %}

## 미리보기 생성

### 1 단계: 지점 체크아웃

터미널에서 사이트 미리보기에 사용할 분기를 확인하세요.

```bash
git checkout BRANCH_NAME
```

바꾸다 `BRANCH_NAME`귀하의 지점 중 하나 또는 다른 사람의 지점 이름으로. 명령은 다음과 유사해야 합니다.

```bash
git checkout BD-2346-fixing-typo-swift
```

### 2 단계: 로컬 서버 시작

로컬 서버를 시작하면[현재 분기](#step-1-checkout-a-branch)의 파일을 사용하여 Braze Docs의 로컬 미리보기를 작성합니다. 현재 분기를 사용하여 로컬 서버를 시작하려면 다음 명령을 실행하세요. `braze-docs`예배 규칙서.

```bash
rake
```

출력은 다음과 유사합니다.

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

### 3단계: 사이트 미리보기 열기

기본적으로 사이트 미리보기는 localhost에서 생성됩니다. [`http://127.0.0.1:4000`](http://127.0.0.1:4000). 사이트 미리보기를 열려면 웹 브라우저에서 링크를 엽니다.

![An example site preview running in a web browser.]({% image_buster /assets/img/contributing/styling_examples/home.png %})

### 4단계: 로컬 서버를 중지하세요

로컬 서버를 중지하려면 터미널을 다시 열고<kbd>Ctrl</kbd>+<kbd>C를</kbd>누르세요.

## 미리보기 업데이트 중

대부분의 경우 파일을 변경하면 사이트 미리보기가 자동으로 업데이트됩니다. `braze-docs`. 이런 일이 발생하면 터미널은 다음과 유사한 메시지를 출력합니다.

```bash
Asset Pipeline: Processing 'javascript_asset_tag' manifest 'global'
Asset Pipeline: Saved 'global-128fd02b54e35ea79fcb21ea460fac06.js' to '/Users/alex-lee/braze-docs/_site/assets'
                    ...done in 1.940883 seconds.
```

브라우저에서 이러한 업데이트를 보려면 페이지를 새로 고치세요.

{% alert tip %}
macOS에서는<kbd>Command</kbd>+<kbd>R을</kbd>, Windows에서는<kbd>Ctrl</kbd>+<kbd>R을</kbd>눌러 브라우저에서 페이지를 새로 고칠 수 있습니다.
{% endalert %}

그러나 다음과 같이 사이트 미리보기가 자동으로 업데이트되지**않는**경우가 있습니다.

- 파일 또는 디렉터리 이름이 변경되었습니다.
- 새 파일이나 디렉터리가 추가되었습니다.
- 파일의 내용은 `_includes`디렉토리가 편집되었습니다 

이러한 업데이트를 보려면[로컬 서버를 중지](#step-4-stop-your-local-server)하고[다시 시작](#step-2-start-a-local-server)해야 합니다.
