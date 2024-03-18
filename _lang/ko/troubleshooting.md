---
nav_title: 문제 해결
article: Troubleshooting
description: "Braze Docs에 기여하는 동안 발생할 수 있는 일반적인 문제에 대한 문제 해결 단계입니다."
page_order: 9
noindex: true
---

# 문제 해결

> Braze Docs에 기여하는 데 문제가 있는 경우 먼저 다음 일반적인 문제를 검토하세요. 겪고 있는 문제가 목록에 없는 경우 여기에 추가할 수 있도록 [알려주세요](https://github.com/braze-inc/braze-docs/issues/new?assignees=&labels=issue&projects=&template=report_an_issue.md&title=).

## 리디렉션이 작동하지 않습니다.

글로벌 리디렉션 파일(`assets/js/broken_redirect_list.js`)에 [설정한 리디렉션이]({{site.baseurl}}/contributing/content_management/redirecting_urls/) 작동하지 않는 경우 URL 문자열에 대문자가 있는지 다시 확인하세요. 파일명을 찾으면 소문자로 변환하세요( `_docs` 디렉터리의 해당 파일명에 대문자가 포함되어 있더라도).

{% tabs local %}
{% tab before %}
```javascript
validurls['/docs/hidden/WIP_Partnerships/WIP_Guidelines'] = '/docs/contributing/home/';
```
{% endtab %}

{% tab after %}
```javascript
validurls['/docs/hidden/wip_partnerships/wip_guidelines'] = '/docs/contributing/home/';
```
{% endtab %}
{% endtabs %}

## 상호 참조 링크가 404를 반환합니다.

페이지의 [상호 참조 링크]({{site.baseurl}}/contributing/content_management/cross_referencing/) (예: `{% raw %}[Braze Developer Guide]({{site.baseurl}}/developer_guide/home){% endraw %}`)가 404 페이지를 반환하는 경우 다음 문자열의 URL을 확인하세요.

```plaintext
%7B%7Bsite.baseurl%7D%7D
```

이 문자열이 포함된 URL은 다음과 유사합니다:

```plaintext
https://www.braze.com/docs/user_guide/personalization_and_dynamic_content/connected_content/%7B%7Bsite.baseurl%7D%7D/user_guide/administrative/app_settings/message_activity_log_tab
```

URL에서 이 문자열을 발견하면 하나 이상의 상호 참조 링크가 [Liquid 원시 태그로](https://shopify.dev/docs/api/liquid/tags/raw) 둘러싸여 있습니다.

{% tabs local %}
{% tab liquid raw tag %}
<code>
{% raw %} {% endraw %}
</code>
{% endtab %}
{% endtabs %}

이러한 태그를 이동하여 원시 콘텐츠로 표시하려는 리퀴드 콘텐츠만 둘러싸도록 합니다.

{% tabs local %}
{% tab before %}
<code>
{% raw %} Liquid의 <code>{{ page\_title }} 태그 사용 방법을 알아보세요. 자세한 내용은 [Liquid 태그를](&#123;&#123;site.baseurl}}/contributing/liquid/) 참조하세요. {% endraw %}
</code>
{% endtab %}

{% tab after %}
<code>
Liquid의 {% raw %} {{ page\_title }} {% endraw %} 태그를 사용하는 방법을 알아보세요. 자세한 내용은 [Liquid 태그를](&#123;&#123;site.baseurl}}/contributing/liquid/) 참조하세요.
</code>
{% endtab %}
{% endtabs %}
