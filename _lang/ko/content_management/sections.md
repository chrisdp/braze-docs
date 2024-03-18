---
nav_title: 섹션
article: Sections
description: "Braze 문서에서 섹션을 만들고 주문하는 방법을 알아보세요."
page_order: 2
noindex: true
---

# 섹션

> Braze 문서에서 섹션을 만들고 주문하는 방법을 알아보세요. 대신 개별 페이지를 생성, 수정 또는 삭제하려면 [페이지를]({{site.baseurl}}/contributing/content_management/pages/) 참조하십시오. 섹션에 대한 일반 정보는 [콘텐츠 관리를]({{site.baseurl}}/contributing/content_management/#sections) 참조하십시오.

{% multi_lang_include contributing/prerequisites.md %}

## 섹션 만들기

### 단계 1: 디렉토리 및 마크다운 파일 생성

관련 기본 섹션 또는 하위 섹션을 연 다음 새 섹션의 디렉터리와 마크다운 파일을 만드세요.

```plaintext
braze-docs
└── _docs
    └── PRIMARY_SECTION 
        └── SUBSECTION 
            ├── NEW_DIRECTORY 
            └── NEW_FILE.md
```

다음을 교체하십시오.

| 플레이스홀더 | 설명 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
`PRIMARY_SECTION`| | 새 콘텐츠가 속한 기본 섹션의 이름입니다. 자세한 내용은 [기본 섹션을]({{site.baseurl}}/contributing/content_management/#primary-sections) 참조하십시오.|
`SUBSECTION`| | 해당하는 경우 새 콘텐츠가 속한 하위 섹션의 이름. 자세한 내용은 [하위 섹션을]({{site.baseurl}}/contributing/content_management/#subsections) 참조하십시오.|
| `NEW_DIRECTORY` | [Braze 문서 스타일]({{site.baseurl}}/contributing/style_guide/) 가이드를 따라야 하는 새 섹션의 이름입니다. 모두 소문자를 사용하고, 특수 문자를 제거하고, 공백을 밑줄 () 로 바꿉니다. `_` 이 이름은 일치해야 합니다`NEW_FILE`.|
| `NEW_FILE` | [Braze 문서 스타일]({{site.baseurl}}/contributing/style_guide/) 가이드를 따라야 하는 새 섹션의 이름입니다. 모두 소문자를 사용하고, 특수 문자를 제거하고, 공백을 밑줄 () 로 바꿉니다. `_` 이 이름은 일치해야 합니다`NEW_DIRECTORY`.|
{: .reset-td-br-1 .reset-td-br-2}

디렉터리 구조는 다음과 비슷해야 합니다.

```plaintext
braze-docs
└── _docs
    └── _developer_guide 
        └── platform_wide 
            ├── getting_started 
            └── getting_started.md
```

### 2단계: 섹션 구성하기

새 섹션을 만들 때 랜딩 페이지를 포함하거나 포함하지 않고 구성할 수 있습니다.

- **랜딩 페이지 포함:** 섹션에 필수 조건을 나열하고 사용자 여정을 요약한 “시작하기” 섹션의 랜딩 페이지와 같이 전용 개요가 필요한 경우 이 방법을 사용하십시오.
- **랜딩 페이지 미포함:** 섹션에 전용 개요가 필요하지 않은 경우 이 방법을 사용하십시오. [Braze Docs 스타일 가이드에]({{site.baseurl}}/contributing/style_guide/) 명시된 바와 같이 콘텐츠는 항상 유용해야 하므로 유용한 콘텐츠를 거의 제공하지 않는 랜딩 페이지를 추가하지 마십시오.

{% tabs %}
{% tab with landing page %}
새 마크다운 파일을 열고 다음 템플릿을 추가합니다. 더 많은 템플릿은 [템플릿을]({{site.baseurl}}/contributing/templates/) 참조하십시오.

\`\`\`마크다운
---
nav_title: 내비게이션\_타이틀
article_title: 랜딩\_페이지\_제목
description: 간략한 설명
---

# 랜딩\_페이지\_제목 

> 간략한 설명

## 표제

함유량
\`\`\`

다음을 교체하십시오.

| 플레이스홀더 | 설명 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
`NAV_TITLE`| | 왼쪽 네비게이션 바에 표시되는 페이지 제목입니다. 대부분의 경우 `nav_title` 일치해야 `article_title` 하지만 공간을 절약하기 위해 더 _짧지만 여전히 비슷한_ 제목을 사용할 수 있습니다.|
| `LANDING_PAGE_TITLE` | 랜딩 페이지의 제목입니다. 메타데이터의 `LANDING_PAGE_TITLE` 값은 검색 엔진 결과에 사용되는 반면 제목 1의 `LANDING_PAGE_TITLE` 값은 페이지에 렌더링된 제목에 사용됩니다.|
| `SHORT_DESCRIPTION` | 페이지에 대한 1-2문장의 짧은 설명입니다. YAML의 메타데이터 `SHORT_DESCRIPTION` 값은 검색 엔진 결과에 사용되는 반면 제목 1 뒤의 `SHORT_DESCRIPTION` 값은 페이지에 렌더링되는 설명에 사용됩니다.|
| `HEADING` | 제목 2 섹션의 제목입니다.|
| `CONTENT` | 제목 2 섹션의 본문 단락입니다.|
{: .reset-td-br-1 .reset-td-br-2}

{% alert tip %}
이 템플릿은 시작하기 위한 용도로만 사용할 수 있습니다. 필요에 따라 [메타데이터와 제목을 추가하세요]({{site.baseurl}}/contributing/yaml_front_matter/metadata/).
{% endalert %}
{% endtab %}

{% tab without landing page %}
하위 섹션의 Markdown 파일을 열고 다음 메타데이터를 추가하여 페이지의 탐색 제목을 설정하고 랜딩 페이지를 비활성화합니다.

\`\`\`마크다운
---
nav_title: 내비게이션\_타이틀
config_only: 참된
---
\`\`\`

{% alert tip %}
이 템플릿은 시작하기 위한 용도로만 사용할 수 있습니다. 필요에 따라 [메타데이터와 제목을 추가하세요]({{site.baseurl}}/contributing/yaml_front_matter/metadata/).
{% endalert %}

왼쪽 네비게이션 바에 표시되는 페이지 `NAV_TITLE` 제목으로 바꾸세요. 페이지는 다음과 비슷해야 합니다.

\`\`\`마크다운
---
nav_title: 시작하기
page_order: 2
noindex: 참된
config_only: 참된
---
\`\`\`
{% endtab %}
{% endtabs %}

### 3단계: 추가 페이지 추가

새 디렉터리에서 각 페이지에 대한 마크다운 파일을 생성합니다. 기본 페이지 레이아웃을 사용하려면 [2단계의]({{site.baseurl}}/contributing/content_management/sections/?tab=with%20landing%20page#step-2-configure-your-section) 템플릿을 사용합니다. 디렉터리 구조는 다음과 비슷해야 합니다.

```plaintext
braze-docs
└── _docs
    └── _developer_guide 
        └── platform_wide 
            ├── getting_started 
            │    ├── integrating_the_sdk.md 
            │    └── setting_up_push_notifications.md
            └── getting_started.md
```

각 페이지에 콘텐츠를 모두 추가했으면 [섹션 주문하기를](#ordering-a-section) 계속 진행하세요.

{% alert tip %}
[페이지에 콘텐츠를 추가하는 방법에 대한 전체 안내는 페이지를 참조하십시오.]({{site.baseurl}}/contributing/content_management/pages/#writing-content)
{% endalert %}

## 섹션 주문하기

섹션을 정렬하려면 해당 섹션에서 Markdown 파일 중 하나를 열고 YAML [`page_order`]({{site.baseurl}}/contributing/yaml_front_matter/metadata/#page-order)서문에서 키를 검색하십시오.

\`\`\`마크다운
---
page_order:
---
\`\`\`

`page_order`키는 왼쪽 탐색 표시줄의 섹션에서 페이지의 상대 순서를 나타내며 음수가 아닌 숫자 (예:, 또는) 로 `0` 설정할 수 있습니다. `20` `5.5` 즉, 현재 디렉터리에 있는 각 Markdown 파일에 `page_order` 대해 알아야 하지만 다른 디렉터리 (하위 디렉터리 포함) 는 알 수 없습니다.

현재 디렉터리에 있는 각 Markdown 파일의 `page_order` 키를 음수가 아닌 숫자로 설정합니다. 다음 예에서는 `page_order` 가 로 설정되어 `2` 있습니다.  

\`\`\`마크다운
---
nav_title: 하위 섹션 B
page_order: 2 
---

# 하위 섹션 B 랜딩 페이지
\`\`\`

출력은 다음과 비슷합니다.

![The left-side navigation on Braze Docs, with the 'Section B' landing page listed third.]({% image_buster /assets/img/contributing/styling_examples/subsection_landing_page.png %})
