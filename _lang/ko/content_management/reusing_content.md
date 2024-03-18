---
nav_title: 콘텐츠 재사용
article: Reusing content
description: "Braze Docs 전체에서 콘텐츠를 재사용하여 콘텐츠 일관성을 개선하고 콘텐츠 제작 시간을 단축하는 방법을 알아보세요."
page_order: 5
noindex: true
---

# 콘텐츠 재사용

> Braze Docs 전체에서 콘텐츠를 재사용하여 콘텐츠 일관성을 개선하고 콘텐츠 제작 시간을 단축하는 방법을 알아보세요. 콘텐츠 재사용에 대한 일반 정보는 [콘텐츠 관리를]({{site.baseurl}}/contributing/content_management/#content-reuse) 참조하십시오.

Jekyll에서의 콘텐츠 재사용은 포함을 사용하여 수행됩니다. 포함은 `_includes` 디렉토리에 일반 Markdown 파일로 저장됩니다. 하지만 `_docs` 디렉터리의 Markdown 파일과 달리 이러한 파일에는 YAML 서문이 필요하지 않습니다.

{% multi_lang_include contributing/prerequisites.md %}

## 포함 만들기

`_includes`디렉터리에 `.md` 확장자가 있는 새 Markdown 파일을 생성합니다. 포함 파일은 이 디렉터리의 아무 곳에나 저장할 수 있지만 하위 디렉터리를 사용하여 관련 콘텐츠를 함께 보관하는 것이 가장 좋습니다. 파일 트리는 다음과 비슷해야 합니다.

```bash
braze-docs
└── _includes
    ├── alerts
    ├── archive
    └── contributing
        └── site_generator.md
```

페이지에 콘텐츠를 추가하고 [Braze 문서 스타일]({{site.baseurl}}/contributing/style_guide/) 가이드를 따르세요. 이미 YAML 서문이 있는 페이지에 포함을 추가할 계획이라면 포함에 머리말을 추가하지 마십시오. 콘텐츠는 다음과 비슷해야 합니다.

{% raw %}
\`\`\`마크다운
## 사이트 생성기 

Braze Docs는 인기 있는 정적 사이트 생성기 (SSG) 인 Jekyll을 사용하여 구축되었습니다. Jekyll을 사용하면 콘텐츠 파일과 디자인 파일을 콘텐츠 파일 및 디자인 파일과 같은 `_docs` 별도의 디렉토리에 저장할 수 있습니다. `assets` 사이트가 구축되면 Jekyll은 각 파일을 지능적으로 병합하여 디렉토리에 XML 및 HTML 데이터로 저장합니다. `_site` 자세한 내용은 [Jekyll 디렉토리](https://jekyllrb.com/docs/structure/) 구조를 참조하십시오.

![The home page for Braze Docs.]({% image_buster /assets/img/contributing/braze_docs_github.png %})

컨트리뷰터는 주로 다음 디렉터리에서 작업하게 됩니다.

| 디렉토리 | 설명 |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`_docs`](https://github.com/braze-inc/braze-docs/tree/develop/_docs)| Braze Docs용으로 작성된 모든 콘텐츠를 마크다운으로 작성된 텍스트 파일로 포함합니다. 텍스트 파일은 [API 섹션 및 [사용 설명서]({{site.baseurl}}/user_guide/introduction) 섹션과]({{site.baseurl}}/api/home) 같이 `_api` 문서 사이트를 미러링하는 디렉터리 및 `user_guide` 하위 디렉터리로 구성됩니다.|
| [`_includes`](https://github.com/braze-inc/braze-docs/tree/develop/_includes)| `_docs` 디렉터리 내 모든 파일에서 재사용할 수 있는 텍스트 파일 (“포함”이라고 함) 이 들어 있습니다. 일반적으로 포함은 표준 서식을 사용하지 않는 짧은 모듈식 콘텐츠입니다. 이 위치에 저장된 파일은 [콘텐츠 재사용에](#content-reuse) 중요합니다.|
| [`assets`](https://github.com/braze-inc/braze-docs/tree/develop/assets)| Braze 문서의 모든 이미지가 포함되어 있습니다. `_docs`또는 `_includes` 디렉터리의 모든 텍스트 파일을 이 디렉터리에 연결하여 해당 페이지에 이미지를 표시할 수 있습니다.|
{: .reset-td-br-1 .reset-td-br-2}
\`\`\`
{% endraw %}

{% alert tip %}
전체 안내는 콘텐츠 [작성을]({{site.baseurl}}/contributing/content_management/pages/#writing-content) 참조하십시오.
{% endalert %}

## 참조 및 포함

포함을 참조하려면 관련 마크다운 파일 내에서 다음 구문을 사용하십시오.

{% raw %}
```plaintext
{% multi_lang_include PATH_TO_INCLUDE %}
```
{% endraw %}

`_includes`디렉토리 내부의 상대 `PATH_TO_INCLUDE` 경로로 바꾸십시오. 예를 들어 다음과 같은 파일 트리가 있습니다.

```bash
braze-docs
└── _includes
    ├── alerts
    ├── archive
    └── contributing
        └── prerequisites.md
```

참조는 다음과 비슷합니다.

{% tabs local %}
{% tab example input %}
{% raw %}
\`\`\`마크다운
# 페이지

> Braze Docs에서 페이지를 만들고, 수정하고, 삭제하는 방법을 알아보세요.

{% multi_lang_include contributing/prerequisites.md %}
\`\`\`
{% endraw %}
{% endtab %}

{% tab example output %}
![Content reuse example on Braze Docs.]({% image_buster /assets/img/contributing/styling_examples/includes.png %}){: style="max-width:90%;"}
{% endtab %}
{% endtabs %}
