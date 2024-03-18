---
nav_title: 이미지
article: Images
description: "Braze 문서에서 이미지를 추가, 수정 및 제거하는 방법을 알아보세요."
page_order: 2
noindex: true
---

# 이미지

> Braze 문서에서 이미지를 추가, 수정 및 제거하는 방법을 알아보세요. 이미지에 대한 일반적인 정보는 [콘텐츠 관리를]({{site.baseurl}}/contributing/content_management/#images) 참조하세요.

{% multi_lang_include contributing/prerequisites.md %}

## 새 이미지 추가하기

### 1단계: 이미지 파일 추가

텍스트 편집기에서 `assets` > `img` 을 엽니다. 일반적으로 새 이미지는 페이지의 다른 이미지와 같은 디렉터리에 추가해야 합니다. 그러나 최선의 판단을 할 수 있습니다. 새 이미지가 [Braze 문서 스타일 가이드를]({{site.baseurl}}/contributing/style_guide/) 따르는지 확인한 다음 관련 하위 디렉터리에 PNG 파일을 추가합니다.

```bash
braze-docs
└── assets
    └── img
        └── DIRECTORY
            └── FILE.png
```

다음을 교체합니다:

| 자리 표시자 | 설명 | 설명
|-------------|-------------------------------------------------------------------------------------------|
| `DIRECTORY` | 관련 디렉토리의 이름입니다. 관련 디렉터리가 없는 경우 디렉터리를 만들 수 있습니다. |
| `FILE` | 파일 확장자를 포함한 파일 이름입니다.                                        |
{: .reset-td-br-1 .reset-td-br-2}

이미지 파일은 다음과 비슷해야 합니다:

```bash
braze-docs
└── assets
    └── img
        └── contributing 
            └── github_home_page.png
```

### 2단계: 이미지 링크

새 이미지에 링크할 때 인라인 또는 참조 스타일 구문을 사용할 수 있습니다. 인라인 구문은 명확성을 우선시하는 반면 참조 스타일 구문은 가독성을 우선시합니다.

{% tabs local %}
{% tab in-line %}
마크다운 파일에서 인라인 구문을 사용하여 새 이미지에 링크합니다.

{% raw %}
```markdown
![ALT_TEXT.]({% image_buster /assets/img/DIRECTORY/IMAGE.png %})
```
{% endraw %}

다음을 교체합니다:

| 자리 표시자 | 설명 | 설명
|-------------|-------------------------------------------------------------------------------------------------------------------------|
| `ALT_TEXT` | 이미지의 대체 텍스트입니다. 이는 화면 리더를 사용하는 사용자도 Braze Docs에 동등하게 액세스할 수 있도록 하기 위해 필요합니다. |
| `IMAGE` | `img` 디렉터리에서 시작하는 이미지의 상대 경로입니다.                                                      |
{: .reset-td-br-1 .reset-td-br-2}

인라인 이미지는 다음과 비슷해야 합니다:

{% raw %}
```markdown
![The form for creating a new pull request on GitHub.]({% image_buster /assets/img/contributing/getting_started/github_pull_request.png %})
```
{% endraw %}
{% endtab %}

{% tab reference-style %}
마크다운 파일에서 참조 스타일 구문을 사용하여 새 이미지에 링크합니다.

{% raw %}
```markdown
![ALT_TEXT.][REFERENCE_NUMBER]
```
{% endraw %}

다음을 교체합니다:

| 자리 표시자 | 설명 | 설명
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| `ALT_TEXT` | 이미지의 대체 텍스트입니다. 이는 화면 리더를 사용하는 사용자도 Braze Docs에 동등하게 액세스할 수 있도록 하기 위해 필요합니다. |
| `REFERENCE_NUMBER` | 이 페이지의 다른 참조 스타일 링크에 아직 할당되지 않은 양의 정수를 지정합니다.                   |
{: .reset-td-br-1 .reset-td-br-2}

인라인 이미지는 다음과 비슷해야 합니다:

{% raw %}
```markdown
![The form for creating a new pull request on GitHub.][10]
```
{% endraw %}

페이지 하단에 참조를 추가합니다.

{% raw %}
```markdown
[REFERENCE_NUMBER]: {{site.baseurl}}SHORT_URL
```
{% endraw %}

다음을 교체합니다:

| 자리 표시자 | 설명 | 설명
|--------------------|---------------------------------------------------------|
| `REFERENCE_NUMBER` | 연결하려는 참조 번호입니다.      |
| `IMAGE` | `img` 디렉터리에서 시작하는 이미지의 상대 경로입니다. |
{: .reset-td-br-1 .reset-td-br-2}

링크는 다음과 유사해야 합니다:

{% raw %}
```markdown
[10]: {% image_buster /assets/img/contributing/getting_started/github_pull_request.png %}
```
{% endraw %}
{% endtab %}
{% endtabs %}

## 이미지 업데이트하기

### 1단계: 원본 참조 찾기

관련 마크다운 파일을 열고 이전 [인라인]({{site.baseurl}}/contributing/content_management/images/?tab=in-line#step-2-link-to-the-image) 또는 [참조 스타일의]({{site.baseurl}}/contributing/content_management/images/?tab=reference-style#step-2-link-to-the-image) 이미지 링크를 찾으면 다음과 유사합니다.

{% raw %}
```markdown
{% image_buster /assets/img/DIRECTORY/IMAGE.png %}
```
{% endraw %}

### 2단계: 이미지 업데이트

기존 이미지를 업데이트할 때는 새 이미지 파일을 추가하거나 기존 이미지 파일을 바꿀 수 있습니다. 새 이미지가 [Braze 문서 스타일 가이드를]({{site.baseurl}}/contributing/style_guide/) 따르는지 확인하세요.

- **기존 파일을 덮어씁니다(권장):** 원본 이미지가 정확한 콘텐츠를 묘사하지만 오래된 브랜딩을 묘사한 이미지와 같이 시각적으로 오래된 경우 이 방법을 사용합니다. 이 방법을 사용하면 Braze Docs 저장소에 저장되는 총 이미지 수가 줄어듭니다.
- **새 파일을 추가합니다:** 원본 이미지가 더 이상 사용되지 않는 기능이나 워크플로를 묘사하는 이미지와 같이 완전히 오래된 콘텐츠를 묘사하는 경우 이 방법을 사용합니다.

{% tabs local %}
{% tab overwrite existing file %}
새 이미지의 이름을 원본 이미지의 이름과 일치하도록 변경합니다. 다음 예제에서는 이미지 파일 이름이 어떻게 동일한지 확인하세요.

- **원본 파일 name:** `getting_started_with_github_select_start3.png`
- **새 파일 name:** `getting_started_with_github_select_start3.png`

그런 다음 새 이미지를 원본 이미지와 같은 디렉터리에 추가합니다. 메시지가 표시되면 이미지를 덮어쓸 것인지 확인합니다. 이미지 파일은 다음과 비슷해야 합니다:

```bash
braze-docs
└── assets
    └── img
        └── contributing 
            └── getting_started_with_github_select_start3.png
```
{% endtab %}

{% tab add new file%}
일반적으로 새 이미지는 이 페이지의 다른 이미지와 동일한 디렉터리에 추가해야 하지만, 최선의 판단을 내릴 수 있습니다. 준비가 완료되면 `assets/img/` 의 해당 위치에 PNG 파일을 추가합니다.

{% alert warning %}
새 이미지 파일을 추가할 때 이전 이미지 파일을 삭제하지 마세요.
{% endalert %}

```bash
braze-docs
└── assets
    └── img
        └── DIRECTORY
            └── FILE.png
```

다음을 교체합니다:

| 자리 표시자 | 설명 | 설명
|-------------|-------------------------------------------------------------------------------------------|
| `DIRECTORY` | 관련 디렉토리의 이름입니다. 관련 디렉터리가 없는 경우 디렉터리를 만들 수 있습니다. |
| `FILE` | 파일 확장자를 포함한 파일 이름입니다.                                        |
{: .reset-td-br-1 .reset-td-br-2}

이미지 파일은 다음과 비슷해야 합니다:

```bash
braze-docs
└── assets
    └── img
        └── contributing 
            └── github_home_page.png
```

이미지를 관련 디렉토리에 추가한 후 [인라인]({{site.baseurl}}/contributing/content_management/images/?tab=in-line#step-2-link-to-the-image) 또는 [참조 스타일]({{site.baseurl}}/contributing/content_management/images/?tab=reference-style#step-2-link-to-the-image) 구문을 사용하여 이 이미지에 링크할 수 있습니다.
{% endtab %}
{% endtabs %}

## 이미지 제거하기

이미지를 제거하려면 관련 마크다운 파일을 열고 [인라인]({{site.baseurl}}/contributing/content_management/images/?tab=in-line#step-2-link-to-the-image) 또는 [참조 스타일]({{site.baseurl}}/contributing/content_management/images/?tab=reference-style#step-2-link-to-the-image) 이미지 링크를 제거합니다. 리포지토리에서 이미지 파일을 삭제하지 마세요.

{% alert warning %}
이미지 파일을 삭제하면 다른 Braze Docs 언어 번역에서 해당 이미지가 손상됩니다.
{% endalert %}
