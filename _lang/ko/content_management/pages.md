---
nav_title: 페이지
article: Pages
description: "Braze Docs에서 페이지를 만들고, 수정하고, 삭제하는 방법을 알아보세요."
page_order: 0
noindex: true
---

# 페이지

> Braze Docs에서 페이지를 만들고, 수정하고, 삭제하는 방법을 알아보세요. 대신 섹션을 만들거나 순서를 변경하려면 [섹션을]({{site.baseurl}}/contributing/content_management/sections/) 참조하십시오. 페이지에 대한 일반 정보는 [콘텐츠 관리를]({{site.baseurl}}/contributing/content_management/#pages) 참조하십시오.

{% multi_lang_include contributing/prerequisites.md %}

## 페이지 만들기

### 단계 1: 새 파일 만들기

관련 디렉터리를 연 다음 페이지에 사용할 새 Markdown 파일을 생성합니다.

```bash
PAGE_TITLE.md
```

[Braze 문서 스타일]({{site.baseurl}}/contributing/style_guide/) 가이드를 따라야 하는 페이지 `PAGE_TITLE` 제목으로 바꾸세요. 모두 소문자를 사용하고, 특수 문자를 제거하고, 공백을 밑줄 () 로 바꿉니다. `_` 파일 이름은 다음과 비슷해야 합니다.

- **페이지:** C++용 개발 환경 title: 설정
- **파일 name:** `setting_up_your_development_environment_for_cpp.md`

{% multi_lang_include contributing/alerts/tip_locating_a_file.md %}

### 2단계: 템플릿 추가

다음 템플릿 중 하나를 복사하여 Markdown 파일에 붙여넣습니다. 자세한 내용은 [템플릿을]({{site.baseurl}}/contributing/templates/) 참조하십시오.

#### 기본 템플릿

{% multi_lang_include contributing/templates/basic.md %}

#### 기술 파트너 템플릿

{% multi_lang_include contributing/templates/technology_partner.md %}

## 콘텐츠 작성

이 섹션에서 다루는 Brase 관련 구문을 제외하고 모든 콘텐츠는 [표준 Markdown](https://www.markdownguide.org/basic-syntax/) 구문을 사용하여 작성됩니다.

### 상호 참조

Braze Docs 외부에서 호스팅되는 페이지를 참조하려면 표준 마크다운 구문을 사용하세요.

{% raw %}
```markdown
[LINK_TEXT](FULL_URL)
```
{% endraw %}

Braze Docs에서 호스팅되는 페이지를 상호 참조하려면 다음과 같은 Braze 관련 구문을 사용하세요.

{% raw %}
```markdown
[LINK_TEXT]({{site.baseurl}}/SHORT_URL)
```
{% endraw %}

{% alert note %}
[전체 안내는 상호 참조를 참조하십시오.]({{site.baseurl}}/contributing/content_management/cross_referencing/)
{% endalert %}

### 이미지 추가

이미지를 추가하려면 이미지의 PNG 파일을 내 `assets/img` 관련 위치에 배치한 후 다음 구문을 사용합니다.

{% raw %}
```markdown
![ALT_TEXT.]({% image_buster /assets/img/DIRECTORY/IMAGE.png %})
```
{% endraw %}

{% alert note %}
전체 안내는 [새 이미지 추가를]({{site.baseurl}}/contributing/content_management/images/) 참조하세요.
{% endalert %}
