---
nav_title: URL 리디렉션
article: Redirecting URLs
description: "Braze Docs에서 페이지 및 페이지 제목의 URL을 리디렉션하는 방법을 알아보세요."
page_order: 6
noindex: true
---

# URL 리디렉션

> Braze Docs에서 페이지 및 페이지 제목의 URL을 리디렉션하는 방법을 알아보세요.

페이지 URL은 항상 Braze Docs 저장소의 디렉터리 구조와 일치합니다. Markdown 파일의 이름이 바뀌거나 다른 디렉터리로 이동되면 리디렉션이 설정되지 않으면 원래 URL에서 404 오류가 발생합니다.

![Example of a 404 page on Braze Docs.]({% image_buster /assets/img/contributing/styling_examples/404.png %})

URL 리디렉션을 설정하면 사용자 북마크가 깨지는 것을 방지할 수 있습니다.

{% multi_lang_include contributing/prerequisites.md %}

## 페이지 리디렉션

페이지의 URL을 Braze Docs 홈 페이지나 새 위치로 리디렉션하도록 선택할 수 있습니다.

{% tabs local %}
{% tab home page %}
관련 Markdown 파일을 열고 다음 키-값 쌍을 YAML 머리말에 추가합니다. 이미 있는 경우 `layout`키를 사용하려면 기존 키를 새 키로 교체하세요.

\`\`마크다운
---
layout: 공백\_구성
---
\`\`\`\`

YAML 머리말은 다음과 유사해야 합니다.

\`\`마크다운
---
nav_title: 사용자 정의 가이드
config_only: 진실
layout: 공백\_구성
page_order: 삼
---
\`\`\`\`
{% endtab %}

{% tab new location %}
관련 Markdown 파일을 이동하거나 이름을 바꾼 후 `assets/js/`디렉터리를 열고 전역 리디렉션 파일을 엽니다.

```bash
braze-docs
└── assets
    └── js
        └── broken_redirect_list.js
```

파일에서 다음 구문을 사용하여 새 줄에 리디렉션을 만듭니다.

```javascript
validurls['REDIRECT_FROM'] = 'REDIRECT_TO';
```

다음을 교체하십시오.

| 자리 표시자 | 설명 |
|----|------------------------------- ------------------------------------- ---------------|
| `REDIRECT_FROM`| 리디렉션_하려는_URL `https://www.braze.com/`URL 문자열에서 제거되었습니다. |
| `REDIRECT_TO`| 리디렉션_하려는_URL `https://www.braze.com/`URL 문자열에서 제거되었습니다. |
{: .reset-td-br-1 .reset-td-br-2}

{% multi_lang_include contributing/alerts/warning_urls_must_be_lowercase.md %}

리디렉션은 다음과 유사해야 합니다.

```javascript
validurls['/docs/user_guide/data_and_analytics/engagement_reports'] = '/docs/user_guide/data_and_analytics/your_reports/engagement_reports';
```
{% endtab %}
{% endtabs %}

## 제목 리디렉션

인페이지 제목의 URL을 리디렉션하려면 `local_redirect`페이지의 YAML 머리말에 있는 키입니다. 먼저 관련 Markdown 파일을 이동하거나 이름을 바꾸고 페이지의 YAML 머리말에서 다음 구문을 사용합니다.

```
local_redirect:
  OLD_HEADING: 'NEW_HEADING_URL'
```

다음을 교체하십시오.

| 자리 표시자 | 설명 |
|------|---------------- ------------------------------------- ------------------------------------- --------------|
| `OLD_HEADING`|[Markdown 구문](https://www.markdownguide.org/basic-syntax/#an-example-putting-the-parts-together)의 이전 제목은 `#`제거됨. |
| `NEW_HEADING_URL`| 리디렉션_하려는_새 제목 URL `https://www.braze.com/`URL 문자열에서 제거되었습니다. |
{: .reset-td-br-1 .reset-td-br-2}

{% multi_lang_include contributing/alerts/warning_urls_must_be_lowercase.md %}

리디렉션은 다음과 유사해야 합니다.

\`\`yaml
---
nav_title: 시작하기
article_title: Braze SDK 시작하기
description: "Braze SDK를 처음 사용하는 경우 시작하는 방법을 알아보세요."
local\_redirect:
  소스에서 빌드: '/docs/developer_guide/getting_started/#using-our-install-script'
\`\`\`\`
