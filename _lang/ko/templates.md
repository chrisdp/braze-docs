---
nav_title: 템플릿
article: Templates
page_order: 4
---

# 템플릿

> 이러한 템플릿을 사용하여 Braze 문서에서 [페이지]({{site.baseurl}}/contributing/content_management/pages/) 또는 [섹션을]({{site.baseurl}}/contributing/content_management/sections/) 만들 수 있습니다.

템플릿의 각 섹션에 대해 자세히 알아보려면 다음과 같은 HTML 주석을 읽어보세요:

'''마크다운
<!-- Here's an HTML comment! -->
```

{% alert important %}
작성하는 동안 이러한 댓글을 파일에 보관할 수 있지만 게시하기 전에 삭제해야 합니다.
{% endalert %}

## 사용 가능한 템플릿

### 기본

{% multi_lang_include contributing/templates/basic.md %}

### 기술 파트너

{% multi_lang_include contributing/templates/technology_partner.md %}

### 릴리스 노트

{% multi_lang_include contributing/templates/release_notes.md %}

## 템플릿 수정하기

이 페이지에 설명된 단계에 따라 템플릿을 수정할 수 있습니다:

- [콘텐츠 관리]({{site.baseurl}}/contributing/content_management/)
- [메타데이터]({{site.baseurl}}/contributing/yaml_front_matter/metadata/)
- [페이지 레이아웃]({{site.baseurl}}/contributing/yaml_front_matter/page_layouts/)
