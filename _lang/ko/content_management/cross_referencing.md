---
nav_title: 상호 참조
article: Cross-referencing
description: "Braze Docs에서 다른 페이지를 상호 참조하는 방법을 알아보세요."
page_order: 4
noindex: true
---

# 상호 참조

> Braze Docs에서 다른 페이지를 상호 참조하는 방법을 알아보세요. Braze Docs 외부 페이지를 상호 참조하려면 [표준](https://www.markdownguide.org/basic-syntax/#links) 마크다운 구문을 사용하세요.

{% multi_lang_include contributing/prerequisites.md %}

## 상호 참조 만들기

상호 참조를 생성할 때는 인라인 방법 또는 참조 스타일 방법을 사용할 수 있습니다. 인라인 방식은 명확성을 우선시하는 반면 참조 스타일 방식은 가독성을 우선시합니다.

{% tabs %}
{% tab in-line %}
관련 마크다운 파일을 연 다음 인라인 링크를 만드세요.

{% subtabs %}
{% subtab Markdown %}

{% raw %}
```markdown
[LINK_TEXT]({{site.baseurl}}/SHORT_URL)
```
{% endraw %}

다음을 교체하십시오.

| 플레이스홀더 | 설명 |
|-------------|--------------------------------------------|
| `LINK_TEXT` | 페이지 제목 또는 관련 작업.|
| `SHORT_URL` | `https://www.braze.com` 제거된 페이지 URL입니다.|
{: .reset-td-br-1 .reset-td-br-2}

인라인 링크는 다음과 비슷해야 합니다.

{% raw %}
```markdown
Before continuing, [create your SSH token]({{site.baseurl}}/docs/developer_guide/platform_wide/sdk_authentication).
```
{% endraw %}
{% endsubtab %}

{% subtab HTML %}

{% raw %}
```markdown
<a href='[SHORT_URL]'>[LINK_TEXT]</a>
```
{% endraw %}

다음을 교체하십시오.

| 플레이스홀더 | 설명 |
|-------------|--------------------------------------------|
| `LINK_TEXT` | 페이지 제목 또는 관련 작업.|
| `SHORT_URL` | `https://www.braze.com` 제거된 페이지 URL입니다.|
{: .reset-td-br-1 .reset-td-br-2}

인라인 링크는 다음과 비슷해야 합니다.

{% raw %}
```markdown
To learn about the different custom attribute data types you can use to segment users, view <a href="/docs/user_guide/data_and_analytics/custom_data/custom_attributes/#custom-attribute-data-types">Custom attribute data types</a>.
```
{% endraw %}
{% endsubtab %}
{% endsubtabs %}

{% endtab %}

{% tab reference-style %}
관련 마크다운 파일을 연 다음 참조 스타일 링크를 만드세요.

```markdown
[LINK_TEXT][REFERENCE_NUMBER]
```

다음을 교체하십시오.

| 플레이스홀더 | 설명 |
|--------------------|----------------------------------------------------------|
| `LINK_TEXT` | 페이지 제목 또는 관련 작업.|
| `REFERENCE_NUMBER` | 이 페이지의 다른 참조 스타일 링크에 아직 할당되지 않은 양의 정수를 할당하세요.|
{: .reset-td-br-1 .reset-td-br-2}

참고 문헌은 다음과 비슷해야 합니다.

```markdown
Before continuing, [create your SSH token][2]. When you're finished, see [Step 2: Uploading your token][5].
```

페이지 하단에 관련 링크를 추가할 수 있습니다.

{% raw %}
```markdown
[REFERENCE_NUMBER]: {{site.baseurl}}SHORT_URL
```
{% endraw %}

다음을 교체하십시오.

| 플레이스홀더 | 설명 |
|--------------------|-------------------------------------------------|
`REFERENCE_NUMBER`| | 링크하려는 문헌의 번호입니다.|
| `SHORT_URL` | `https://www.braze.com/docs` 제거된 페이지 URL입니다.|
{: .reset-td-br-1 .reset-td-br-2}

링크는 다음과 비슷해야 합니다.

{% raw %}
```markdown
[2]: {{site.baseurl}}/developer_guide/platform_wide/sdk_authentication/
[5]: {{site.baseurl}}/developer_guide/platform_wide/swift#step-2-uploading-your-token
```
{% endraw %}
{% endtab %}
{% endtabs %}
