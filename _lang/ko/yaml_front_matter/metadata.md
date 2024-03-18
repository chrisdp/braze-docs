---
nav_title: 메타데이터
article: Metadata
description: "페이지의 YAML 서문에 추가할 수 있는 메타데이터 키입니다."
page_order: 0
noindex: true
---

#  메타데이터

> 페이지의 YAML 서문에 추가할 수 있는 메타데이터 키입니다. 보다 일반적인 정보는 [콘텐츠 관리를]({{site.baseurl}}/contributing/content_management/#pages) 참조하십시오.

마크다운 파일에 메타데이터를 추가하려면 파일 시작 부분에 Jekyll의 머리말 구문을 추가해야 합니다.

\`\`\`마크다운
---
메타데이터\_키: 메타데이터\_값
---

# 브레이즈 문서 시작하기

Braze Docs 또는 Docs-as Code를 처음 사용하는 경우 튜토리얼부터 시작하세요.
\`\`\`

다음을 교체하십시오.

| 플레이스홀더 | 설명 |
|-------------------------------------------------------------------------------------------------------------------------------------------|
| `METADATA_KEY` | 지원되는 메타데이터 유형을 나타내는 키입니다. 다음 섹션의 [메타데이터 키로](#required-keys) 대체합니다.|
| `METADATA_VALUE` | 메타데이터 키에 할당된 값입니다. 다음 섹션에서 메타데이터 키의 지원되는 값을 확인하세요.|
{: .reset-td-br-1 .reset-td-br-2}

## 필수 키

### 기사 제목

`article_title`키는 온라인 검색 결과의 페이지 제목과 최종 사용자의 브라우저 탭을 설정하는 데 사용됩니다. 이 키는 모든 `string` 값을 허용합니다. 이름 지정 규칙은 [Braze 문서]({{site.baseurl}}/contributing/style_guide/) 스타일 가이드를 참조하십시오.

{% tabs local %}
{% tab usage example %}
\`\`\`마크다운
---
article_title: 브레이즈 문서 시작하기
---
\`\`\`
{% endtab %}
{% endtabs %}

### 설명

`description`키는 온라인 검색 결과에서 페이지 설명을 설정하는 데 사용됩니다. 이 키는 큰따옴표로 둘러싸인 150자 미만의 모든 `string` 값을 허용합니다.

{% tabs local %}
{% tab usage example %}
\`\`\`마크다운
---
description: “Braze Docs를 처음 사용하는 경우 이 단계별 자습서부터 시작하세요.”
---
\`\`\`
{% endtab %}
{% endtabs %}

### 내비게이션 제목

`nav_title`키는 Braze Docs의 왼쪽 탐색 표시줄에서 페이지 제목을 설정하는 데 사용됩니다. 이 키는 30자 `string` 미만을 입력할 수 있습니다. [`hidden`](#hide-page-from-navigation)키가 로 설정된 `true` 경우에는 `nav_title` 필요하지 않습니다.

{% tabs local %}
{% tab usage example %}
\`\`\`마크다운
---
nav_title: 시작하기
---
\`\`\`
{% endtab %}
{% endtabs %}

## 옵션 키

### 인게이지먼트 툴

`tool`키는 페이지의 관련 참여 도구를 설정하는 데 사용됩니다. 이 키는 다음 `string` 값 중 하나 이상을 목록으로 받아들입니다.

- `dashboard`
- `docs`
- `canvas`
- `campaigns`
- `currents`
- `location`
- `media`
- `reports`
- `segments`
- `templates`

{% tabs local %}
{% tab usage example %}
\`\`\`마크다운
---
tool:
  \- 전류
  \- 세그먼트
---
\`\`\`
{% endtab %}
{% endtabs %}

### 탐색에서 페이지 숨기기

`hidden`키는 Braze Docs의 왼쪽 탐색에서 페이지를 숨기는 데 사용됩니다. 이 키는 부울 값 `true` 또는 `false` 을 허용합니다.

{% tabs local %}
{% tab usage example %}
\`\`\`마크다운
---
hidden: 참된
---
\`\`\`
{% endtab %}
{% endtabs %}

### 검색에서 페이지 숨기기

`noindex`키는 내부 및 외부 검색결과 (예: Braze Docs 및 Google 검색) 에서 페이지를 숨기는 데 사용됩니다. 이 키는 부울 값 `true` 또는 `false` 을 허용합니다.

{% tabs local %}
{% tab usage example %}
\`\`\`마크다운
---
noindex: 참된
---
\`\`\`
{% endtab %}
{% endtabs %}

### 목차 숨기기

`hide_toc`키는 페이지 오른쪽에 있는 페이지 내 목차 (TOC) 를 숨기는 데 사용됩니다. 이 키는 부울 값 `true` 또는 `false` 을 허용합니다.

{% tabs local %}
{% tab usage example %}
\`\`\`마크다운
---
hide_toc: 참된
---
\`\`\`
{% endtab %}
{% endtabs %}

### 목차에서 제목 숨기기

`toc_headers`키는 페이지 오른쪽에 있는 페이지 내 목차 (TOC) 에서 동일한 수준의 모든 제목을 숨기는 데 사용됩니다. 이 키는 다음 문자열 값을 받아들입니다.

- `h1`
- `h2`
- `h3`
- `h4`

`toc_headers` 지정된 값과 일치하는 모든 제목을 숨깁니다. 목차에서 특정 제목을 숨기는 데 사용할 수 없습니다.

{% tabs local %}
{% tab usage example %}
\`\`\`마크다운
---
토크\_헤더: h2
---
\`\`\`
{% endtab %}
{% endtabs %}

### 메시징 채널

`channel`키는 페이지의 관련 메시징 채널을 설정하는 데 사용됩니다. 이 키는 다음 `string` 값 중 하나 이상을 목록으로 받아들입니다.

- `content cards`
- `email`
- `in-app messages`
- `news feed`
- `push`
- `sms`
- `webhooks`

{% tabs local %}
{% tab usage example %}
\`\`\`마크다운
---
채널:
  \- 이메일
  \- 뉴스 피드
---
\`\`\`
{% endtab %}
{% endtabs %}

### 내비게이션 전용

`config_only`키는 왼쪽 탐색 모음에 페이지를 숨기지 않고 페이지의 콘텐츠를 숨기는 데 사용됩니다. [랜딩 페이지가 없는 섹션을 만들]({{site.baseurl}}/contributing/content_management/sections?tab=without%20landing%20page#step-2-configure-your-section) 때 이 키를 사용하십시오. 이 키는 부울 값 `true` 또는 `false` 을 허용합니다.

{% tabs local %}
{% tab usage example %}
\`\`\`마크다운
---
config_only: 참된
---
\`\`\`
{% endtab %}
{% endtabs %}

### 기본 URL 재정의

`permalink`키는 Braze Docs 페이지의 기본 URL을 재정의하는 데 [`hidden`](#hide-page-from-navigation)키와 함께 사용됩니다. 리디렉션하기 `https://www.braze.com/docs` 전에 에 할당된 값이 앞에 `permalink` 추가됩니다. 이 키는 다음 요구 사항을 충족하는 모든 `string` 값을 허용합니다.

- 문자는 소문자입니다
- 단어는 밑줄 () `_` 로 구분합니다.
- “디렉토리”는 슬래시 () 로 구분됩니다. `/`
- 다른 모든 특수 문자는 제거됩니다.

{% tabs local %}
{% tab usage example %}
\`\`\`마크다운
---
hidden: 참된
permalink: /support_contact/docs_team/
---
\`\`\`
{% endtab %}
{% endtabs %}

### 페이지 레이아웃

`layout`키는 페이지의 레이아웃을 설정하는 데 사용됩니다. 설정하지 않으면 `layout` `default` 레이아웃이 사용됩니다. 이 키는 다음 `string` 값 중 하나를 허용합니다.

- `api_page`
- `dev_guide`
- `featured_video`
- `featured`
- `glossary_page`
- `blank_config`
- `redirect`

각 값에 대한 자세한 내용은 [페이지 레이아웃을]({{site.baseurl}}/contributing/yaml_front_matter/page_layouts/) 참조하십시오.

{% tabs local %}
{% tab usage example %}
\`\`\`마크다운
---
page_layout: 용어집 페이지
---
\`\`\`
{% endtab %}
{% endtabs %}

### 페이지 순서

`page_order`키는 왼쪽 탐색 모음에서 [섹션을 정렬하는]({{site.baseurl}}/contributing/content_management/sections/#ordering-a-section) 데 사용됩니다. 이 키에는 음수가 아닌 모든 숫자 (예: `0``20`, 또는`5.5`) 를 사용할 수 있습니다.

{% tabs local %}
{% tab usage example %}
\`\`\`마크다운
---
page_order: 35.6
---
\`\`\`
{% endtab %}
{% endtabs %}

### 페이지 유형

`page_type`키는 페이지의 서식을 설정하는 데 사용됩니다. 이 키는 다음 `string` 값 중 하나를 허용합니다.

- `glossary`
- `solution`
- `reference`
- `tutorial`
- `landing`
- `partner`
- `update`

각 값에 대한 자세한 내용은 [페이지 유형을]({{site.baseurl}}/contributing/yaml_front_matter/page_layouts/) 참조하십시오.

{% tabs local %}
{% tab usage example %}
\`\`\`마크다운
---
page_type: 지도서
---
\`\`\`
{% endtab %}
{% endtabs %}

### 플랫폼

`platform`키는 페이지의 관련 플랫폼을 설정하는 데 사용됩니다. 이 키는 하나 이상의 [Braze SDK를]({{site.baseurl}}/developer_guide/home/) 목록의 `string` 값으로 받아들입니다.

{% tabs local %}
{% tab usage example %}
\`\`\`마크다운
---
플랫폼:
  \- iOS
  \- 웹
  \- 안드로이드
---
\`\`\`
{% endtab %}
{% endtabs %}
