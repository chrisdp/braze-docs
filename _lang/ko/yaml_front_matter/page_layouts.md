---
nav_title: 페이지 레이아웃
article: Page layouts
description: "다음은 페이지의 YAML 앞부분에 있는 `page_layout` 키에 할당할 수 있는 페이지 레이아웃입니다."
page_order: 2
noindex: true
---

#  페이지 레이아웃

> 다음은 페이지의 YAML 앞부분에서 키에 할당할 수 있는 페이지 레이아웃입니다. [`page_layout`]({{site.baseurl}}/contributing/yaml_front_matter/metadata/#page-layout) 키에 할당할 수 있는 페이지 레이아웃입니다. 자세한 내용은 [콘텐츠 관리를]({{site.baseurl}}/contributing/content_management/#layouts) 참조하세요.

## 전제 조건

페이지 레이아웃을 사용하려면 YAML 앞부분에 [`page_layout`]({{site.baseurl}}/contributing/yaml_front_matter/metadata/#page-layout) 키를 추가해야 합니다.

'''마크다운
---
nav_title: 시작하기
article_title: Braze 문서 시작하기
page_layout: 페이지\_레이아웃\_값
---
\`\`\`

`PAGE_LAYOUT_VALUE` 을 다음 섹션의 값 중 하나로 바꿉니다.

## 시각적 레이아웃

### API 페이지

`api_page` 값은 API 페이지 형식을 적용하는 데 사용됩니다. 다음 예에서는 이 형식을 [목록 연동]({{site.baseurl}}/api/endpoints/cdi/get_integration_list/) 페이지에 적용합니다:

{% tabs local %}
{% tab example output %}
![An example page using the 'api_page' layout.]({% image_buster /assets/img/contributing/styling_examples/layouts/api_page.png %})
{% endtab %}
{% endtabs %}

### 개발자 가이드

`dev_guide` 값은 개발자 가이드 형식을 적용하는 데 사용됩니다. 다음 예제에서는 이 형식을 [카탈로그 엔드포인트]({{site.baseurl}}/api/endpoints/catalogs) 페이지에 적용합니다: 

{% tabs local %}
{% tab example output %}
![An example page using the 'dev_guide' layout.]({% image_buster /assets/img/contributing/styling_examples/layouts/dev_guide.png %})
{% endtab %}
{% endtabs %}

### 추천 페이지

`featured` 값은 추천 페이지 형식을 적용하는 데 사용됩니다. 다음 예에서는 이 형식을 [예측 이벤트]({{site.baseurl}}/user_guide/sage_ai/predictive_suite/predictive_events) 페이지에 적용합니다:

{% tabs local %}
{% tab example output %}
![An example page using the 'featured' layout.]({% image_buster /assets/img/contributing/styling_examples/layouts/featured.png %})
{% endtab %}
{% endtabs %}

### 용어집 페이지

`glossary_page` 값은 용어집 페이지 형식을 적용하는 데 사용됩니다. 다음 예에서는 이 형식이 [푸시 알림 유형]({{site.baseurl}}/user_guide/message_building_by_channel/push/types) 페이지에 적용됩니다:

{% tabs local %}
{% tab example output %}
![An example page using the 'glossary_page' layout.]({% image_buster /assets/img/contributing/styling_examples/layouts/glossary_page.png %})
{% endtab %}
{% endtabs %}

{% alert tip %}
특정 레이아웃에서 `"guide_top_text:"` 같은 값은 마크다운 서식을 사용하면 이점이 있을 수 있습니다. 특정 YAML 값에 마크다운 서식을 사용할 수 있습니다. 이렇게 하려면 `>` 을 YAML 값으로 추가하고 그 뒤에 텍스트를 들여쓰기합니다.
<br>
예를 들어<br>
가이드\_상단\_텍스트: ><br>
    \# 마크다운 서식 지정 예시입니다.
{% endalert %}

## 기타 레이아웃

### 빈 구성

`blank_config` 값은 브레이즈 문서에서 페이지를 숨기고 사용자를 `www.braze.com/docs` 으로 자동 리디렉션하는 데 사용됩니다. 자세한 내용은 [URL 리디렉션을]({{site.baseurl}}/contributing/content_management/redirecting_urls/?tab=home%20page#redirecting-a-page) 참조하세요.

### 리디렉션

`redirect` 값은 페이지 내 제목의 URL을 리디렉션하는 데 사용됩니다. 자세한 내용은 [URL 리디렉션을]({{site.baseurl}}/contributing/content_management/redirecting_urls/#redirecting-a-heading) 참조하세요.
