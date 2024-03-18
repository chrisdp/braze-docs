---
nav_title: 스타일링 예시
article: Styling examples
description: "머리글, 탭, 코드 블록 등 Braze 문서에서 페이지 스타일이 지정되는 방식입니다."
page_order: 8 
noindex: true
---

# 스타일링 예시

머리글, 탭, 코드 블록 등 Braze 문서에서 페이지 스타일이 지정되는 방식입니다.

## 헤더 테스트

{% tabs %}
{% tab Styling %}

# H1 배너
H1 텍스트

로렘 입섬 돌로르 시트 아멧, 컨설턴트 아디피싱 엘리트. Sed nec tortor at lectus tempus tempor. 서스펜디세 텔루스 디암, 피니버스 에우 딕텀 논, 베리에이션 및 입섬.

## H2 배너
H2 텍스트

로렘 입섬 돌로르 시트 아멧, 컨설턴트 아디피싱 엘리트. Sed nec tortor at lectus tempus tempor. 서스펜디세 텔루스 디암, 피니버스 에우 딕텀 논, 베리에이션 및 입섬.

### H3 배너
H3 텍스트

로렘 입섬 돌로르 시트 아멧, 컨설턴트 아디피싱 엘리트. Sed nec tortor at lectus tempus tempor. 서스펜디세 텔루스 디암, 피니버스 에우 딕텀 논, 베리에이션 및 입섬.

#### H4 배너
H4 텍스트

로렘 입섬 돌로르 시트 아멧, 컨설턴트 아디피싱 엘리트. Sed nec tortor at lectus tempus tempor. 서스펜디세 텔루스 디암, 피니버스 에우 딕텀 논, 베리에이션 및 입섬.

##### H5 배너
H5 텍스트

로렘 입섬 돌로르 시트 아멧, 컨설턴트 아디피싱 엘리트. Sed nec tortor at lectus tempus tempor. 서스펜디세 텔루스 디암, 피니버스 에우 딕텀 논, 베리에이션 및 입섬.

###### H6 배너
H6 텍스트

로렘 입섬 돌로르 시트 아멧, 컨설턴트 아디피싱 엘리트. Sed nec tortor at lectus tempus tempor. 서스펜디세 텔루스 디암, 피니버스 에우 딕텀 논, 베리에이션 및 입섬.

{% endtab %}
{% tab Markdown %}

\`\`\`
# H1 배너

## H2 배너

### H3 배너

#### H4 배너

##### H5 배너

###### H6 배너
\`\`\`
{% endtab %}
{% endtabs %}

## 사용자 지정 헤더 앵커

제목에 앵커를 추가하려면 제목이 있는 줄 끝에 다음 코드를 추가합니다. `anchor-text` 을 이 제목의 앵커로 바꿉니다. 소문자를 사용하고 단어 사이에 하이픈을 넣습니다.

\`\`\`
# 제목 텍스트 {#anchor-text}
\`\`\`

숫자 기호 `#` 뒤에 사용자 정의 앵커를 붙인 표준 링크를 만들어 사용자 정의 앵커를 사용하여 제목에 연결할 수 있습니다.

{% raw %}
```
Here is my [link](#anchor-text)
```
{% endraw %}

## 글꼴 테스트

{% tabs %}
{% tab Styling %}

일반 텍스트

*텍스트 강조*

**Bold**

_**굵게 강조**_

~~ 취소선~~

{% endtab %}
{% tab Markdown %}
\`\`\`
일반 텍스트

*텍스트 강조*

**Bold**

_**굵게 강조**_

~~ 취소선~~
\`\`\`
{% endtab %}
{% endtabs %}

## 견적 테스트

{% tabs %}
{% tab Styling %}
> 인용된 텍스트

#### 인라인 견적
Lorem ipsum dolor ``sit amet, consectetur adipiscing elit``. Sed nec tortor at lectus tempus tempor.

#### 견적 청크
```
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nec tortor at lectus tempus tempor.
```
{% endtab %}
{% tab Markdown %}
\`\`\`
> 인용된 텍스트

Lorem ipsum dolor ``sit amet, consectetur adipiscing elit``. Sed nec tortor at lectus tempus tempor.

``` Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nec tortor at lectus tempus tempor. ```
\`\`\`
{% endtab %}
{% endtabs %}

## 테이블 테스트

{% tabs %}
{% tab Styling %}
인스턴스 | 대시보드 URL | REST 엔드포인트
----------- |---------------- | --------------------
US-01 | `https://dashboard.braze.com` 또는<br> `https://dashboard-01.braze.com` | `https://rest.iad-01.braze.com`
US-02 | `https://dashboard-02.braze.com` | `https://rest.iad-02.braze.com`
US-03 | `https://dashboard-03.braze.com` | `https://rest.iad-03.braze.com`
US-04 | `https://dashboard-04.braze.com` | `https://rest.iad-04.braze.com`
US-05 | `https://dashboard-05.braze.com` | `https://rest.iad-05.braze.com`
US-06 | `https://dashboard-06.braze.com` | `https://rest.iad-06.braze.com`
US-07 | `https://dashboard-07.braze.com` | `https://rest.iad-07.braze.com`
US-08 | `https://dashboard-08.braze.com` | `https://rest.iad-08.braze.com`
EU-01 | `https://dashboard.braze.eu` 또는<br> `https://dashboard-01.braze.eu` | `https://rest.fra-01.braze.eu`
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}
{% endtab %}
{% tab Markdown %}
```
Instance    | Dashboard URL   | REST Endpoint
----------- |---------------- | --------------------
US-01 | `https://dashboard.braze.com` or<br> `https://dashboard-01.braze.com` | `https://rest.iad-01.braze.com`
US-02 | `https://dashboard-02.braze.com` | `https://rest.iad-02.braze.com`
US-03 | `https://dashboard-03.braze.com` | `https://rest.iad-03.braze.com`
US-04 | `https://dashboard-04.braze.com` | `https://rest.iad-04.braze.com`
US-05 | `https://dashboard-05.braze.com` | `https://rest.iad-05.braze.com`
US-06 | `https://dashboard-06.braze.com` | `https://rest.iad-06.braze.com`
US-07 | `https://dashboard-07.braze.com` | `https://rest.iad-07.braze.com`
US-08 | `https://dashboard-08.braze.com` | `https://rest.iad-08.braze.com`
EU-01 | `https://dashboard.braze.eu` or<br> `https://dashboard-01.braze.eu` | `https://rest.fra-01.braze.eu`
EU-02 | `https://dashboard-02.braze.eu` | `https://rest.fra-02.braze.eu`
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3}
```
{% endtab %}
{% endtabs %}

#### 열별 표 단어 나누기 재설정
단어 나누기를 기본 스타일로 재설정해야 하는 테이블 열의 경우 마크다운 옵션을 사용하여 `.reset-td-br-1`, `.reset-td-br-2`, `.reset-td-br-3`, `.reset-td-br-4`, `#` 를 사용하여 테이블에 클래스를 추가하고 열에 해당하는 는 최대 4까지 입력합니다.

#### 사용법
\`\`\`
| 이벤트 이름 | 피드 유형 | 설명 | 사용자 지정 속성
| ------------------------------------ | ---------------------- | ----------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| 언브레이킹된 단어가 오래됨언브레이킹된 단어가 오래됨 | 언바운드 피드 | 이메일이 사용자의 메일 서버로 성공적으로 전달되었습니다.                              | `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id` |
| `UNBROKENHIGHLIGHTTHATISVERYLONGUNBROKENHIGHLIGHTTHATISVERYLONG` | 언바운드 피드 | 사용자가 이메일을 열었습니다.                                                                     | `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id` |
| 인앱 메시지 노출 > 플랫폼별 피드 > 사용자가 인앱 메시지를 조회했습니다.                                                            | `app_id`, `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id` |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

\`\`\`
{% tabs local %}
{% tab Before %}

| 이벤트 이름 | 피드 유형 | 설명 | 사용자 지정 속성 | 사용자 지정 속성
|------------------------------------------------------------------|------------------------|--------------------------------------------------------------|-------------------------------------------------------------------------------|
| 언브레이킹된 단어가 오래됨언브레이킹된 단어가 오래됨 | 언바운드 피드 | 이메일이 사용자의 메일 서버로 성공적으로 전달되었습니다. | `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id` |
| `UNBROKENHIGHLIGHTTHATISVERYLONGUNBROKENHIGHLIGHTTHATISVERYLONG` | 언바운드 피드 | 사용자가 이메일을 열었습니다.                                        | `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id` |
| 인앱 메시지 노출 | 플랫폼별 피드 | 사용자가 인앱 메시지를 조회했습니다.                               | `app_id`, `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id` |

{% endtab %}
{% tab After %}

| 이벤트 이름 | 피드 유형 | 설명 | 사용자 지정 속성 | 사용자 지정 속성
|------------------------------------------------------------------|------------------------|--------------------------------------------------------------|-------------------------------------------------------------------------------|
| 언브레이킹된 단어가 오래됨언브레이킹된 단어가 오래됨 | 언바운드 피드 | 이메일이 사용자의 메일 서버로 성공적으로 전달되었습니다. | `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id` |
| `UNBROKENHIGHLIGHTTHATISVERYLONGUNBROKENHIGHLIGHTTHATISVERYLONG` | 언바운드 피드 | 사용자가 이메일을 열었습니다.                                        | `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id` |
| 인앱 메시지 노출 | 플랫폼별 피드 | 사용자가 인앱 메시지를 조회했습니다.                               | `app_id`, `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id` |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}
{% endtab %}
{% endtabs %}

## 링크 테스트
{% tabs %}
{% tab Styling %}
여기를 클릭하세요: [Braze.com](https://www.braze.com){: height="36px" width="36px"}
{% endtab %}
{% tab Markdown %}
```
[Braze.com](https://www.braze.com)
```
{% endtab %}
{% endtabs %}

## 이미지 테스트
{% tabs %}
{% tab Styling %}
이미지: ![Logo]({% image_buster /assets/img/braze-logo-mark.png %}){: style="max-width:30%;"}

#### 링크된 이미지 테스트

링크된 이미지: [![Braze]({% image_buster /assets/img/braze-logo-mark.png %}){: style="max-width:30%;"}](https://www.braze.com)

#### 이미지 스타일링

![Text]({% image_buster /assets/img/logo-braze-fa.svg %}){: style="max-width:30%; color: green" }

#### 이미지 앵커링

![Text]({% image_buster /assets/img/logo-braze-fa.svg %}){: style="float:right;max-width:30%; color: green" }
<br><br><br><br><br>
{% endtab %}
{% tab Markdown %}

\`\`\`
![Logo]({% image_buster /assets/img/braze-logo-mark.png %}){: style="max-width:30%;"}

[![Braze]({% image_buster /assets/img/braze-logo-mark.png %})](https://www.braze.com)

![Text]({% image_buster /assets/img/logo-braze-fa.svg %}){: style="max-width:30%; color: green" }

![Text]({% image_buster /assets/img/logo-braze-fa.svg %}){: style="float:right;max-width:30%;" }
\`\`\`
{% endtab %}
{% endtabs %}

## 갤러리 테스트
{% tabs %}
{% tab Styling %}
{% gallery %}
{{site.baseurl}}/assets/img_archive/EBTH_Email.png?bf892368baf287cba5ab9a6e3b09431d <br> [링크입니다](https://www.braze.com).
{{site.baseurl}}/assets/img_archive/iHeartRadio_Email.png?ecd2c8fe148939b7de957fe85cd6317e <br> 이것은 또 다른 `comment` 입니다.
{{site.baseurl}}/assets/img_archive/Saucey_Email.png?b9768937a1cc12d4c08e55a52e700d68 <br> 또 다른 **댓글입니다**.
{{site.baseurl}}/assets/img/schellman_iso27001_seal_grey_CMYK_300dpi_jpg.png?1b1fb9dbb80b0332c62512dcf9c83258 <br> **이미지 제목** <br> 줄 바꿈이 발생하는지 확인하는 테스트입니다.
{{site.baseurl}}/assets/img/SOC2.png?6338040be8e98c4c9abe1f35b3e43e3a <br> 이것은 일반적인 댓글입니다.
{% endgallery %}
{% endtab %}
{% tab Markdown %}
{% raw %}
```
{% gallery %}
{{site.baseurl}}/assets/img_archive/EBTH_Email.png?bf892368baf287cba5ab9a6e3b09431d  <br> This is a [link](https://www.braze.com).
{{site.baseurl}}/assets/img_archive/iHeartRadio_Email.png?ecd2c8fe148939b7de957fe85cd6317e  <br> This is another `comment`.
{{site.baseurl}}/assets/img_archive/Saucey_Email.png?b9768937a1cc12d4c08e55a52e700d68  <br> This is yet another **comment**.
{{site.baseurl}}/assets/img/schellman_iso27001_seal_grey_CMYK_300dpi_jpg.png?1b1fb9dbb80b0332c62512dcf9c83258 <br> **IMAGE TITLE** <br> This is a test to see if it will line break.
{{site.baseurl}}/assets/img/SOC2.png?6338040be8e98c4c9abe1f35b3e43e3a  <br> This is a regular comment.
{% endgallery %}
```
{% endraw %}
{% endtab %}
{% endtabs %}

## 인터랙티브 이미지 테스트
{% tabs %}
{% tab Styling %}
<div class="iactiveImg" data-ii="6967"></div><script src="https://interactive-img.com/js/include.js"></script>
{% endtab %}
{% tab Markdown %}
```
<div class="iactiveImg" data-ii="6967"></div><script src="https://interactive-img.com/js/include.js"></script>
```
{% endtab %}
{% endtabs %}
<!--- Leaving formatting here just in case it's important...
<div style="position: relative; padding-bottom: 83%; padding-top: 0; height: 0;"><iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border-width:0px; max-width:100%; overflow-y:auto;" width="100%" height="100%" src="https://interactive-img.com/view?id=6967&iframe=true"></iframe></div>
-->

## 코드 스니펫 테스트

{% tabs %}
{% tab Styling %}
#### 코드 테스트 목표 C
```objc
- (void)submitFeedback:(ABKFeedback * )feedback
 withCompletionHandler:(nullable void (^)(ABKFeedbackSentResult feedbackSentResult))completionHandler;
```

#### 코드 테스트 스위프트
```swift
Appboy.sharedInstance()?.submitFeedback(feedback) { (feedbackSentResult) in
      print("Feedback sent: (feedbackSentResult)")
    }
```

#### 코드 테스트 Java
```java
@Override
public void onResume() {
  super.onResume();
  // Registers the BrazeInAppMessageManager for the current Activity. This Activity will now listen for
  // in-app messages from Braze.
  BrazeInAppMessageManager.getInstance().registerInAppMessageManager(activity);
}
```

#### 코드 테스트 json
```json
{
   "attributes" : "Attributes" ,
   "events" : ["Array", "Of", "Object"],
   "purchases" : ["Array" ,"Of" ,"Purchase" ,"Object"]
}
```

#### 자바스크립트 코드 테스트
```javascript
braze.subscribeToFeedUpdates(function(feed) {
  var cards = feed.cards;
  braze.showFeed(undefined, cards);
});
braze.requestFeedRefresh();
```

#### 파이그먼트 테스트
\`\`\`python
\#!/usr/bin/python3

엔진에서 런포레스트런을 가져옵니다.

"""구문 강조를 위한 테스트 코드!"""

클래스 Foo:
	def __init__(self, var):
		self.var = var
		self.run()

	def run(self):
		RunForrestRun()  # run along!

\`\`\`
{% endtab %}
{% tab Markdown %}
![Markdown Example]({% image_buster /assets/img_archive/code_snippet.png %})
{% endtab %}
{% endtabs %}

## 알림 테스트

{% tabs %}
{% tab Styling %}

{% alert tip %}다음은 팁입니다.{% endalert %}

{% alert note %}참고 사항{% endalert %}

{% alert important %}이것은 중요한 알림입니다.{% endalert %}

{% alert warning %}이것은 경고입니다.{% endalert %}

{% alert update %}업데이트 내용입니다.{% endalert %}

{% endtab %}
{% tab Markdown %}
{% raw %}
\`\`\`
{% alert tip %}
다음은 팁입니다.
{% endalert %}

{% alert note %}
참고 사항
{% endalert %}

{% alert important %}
이것은 중요한 알림입니다.
{% endalert %}

{% alert warning %}
이것은 경고입니다.
{% endalert %}

{% alert update %}
업데이트 내용입니다.
{% endalert %}
\`\`\`
{% endraw %}
{% endtab %}
{% endtabs %}

## 임베디드 비디오 테스트
{% tabs %}
{% tab Styling %}
#### 임베디드 동영상/유튜브
기본값은 YouTube 임베드입니다.
{% multi_lang_include video.html id="XY5vFY" source="youtube" %}

#### 임베디드 비디오 오른쪽 정렬
{% multi_lang_include video.html id="XYuXoKIvFY" align="right" source="youtube" %}

로렘 입섬 돌로르 시트 아멧, 컨설턴트 아디피싱 엘리트. Sed nec tortor at lectus tempus tempor. 서스펜디세 텔루스 디암, 피니버스 에우 딕텀 논, 베리에이션 및 입섬. 로렘 입섬 돌로르 시트 아멧, 컨설턴트 아디피싱 엘리트. Sed nec tortor at lectus tempus tempor. 서스펜디세 텔루스 디암, 피니버스 에우 딕텀 논, 베리에이션 및 입섬. 로렘 입섬 돌로르 시트 아멧, 컨설턴트 아디피싱 엘리트. Sed nec tortor at lectus tempus tempor. 서스펜디세 텔루스 디암, 피니버스 에우 딕텀 논, 베리에이션 및 입섬.

#### 임베디드 비디오 왼쪽 정렬
{% multi_lang_include video.html id="XY5uXvFY" align="left" source="youtube" %}

로렘 입섬 돌로르 시트 아멧, 컨설턴트 아디피싱 엘리트. Sed nec tortor at lectus tempus tempor. 서스펜디세 텔루스 디암, 피니버스 에우 딕텀 논, 베리에이션 및 입섬. 로렘 입섬 돌로르 시트 아멧, 컨설턴트 아디피싱 엘리트. Sed nec tortor at lectus tempus tempor. 서스펜디세 텔루스 디암, 피니버스 에우 딕텀 논, 베리에이션 및 입섬. 로렘 입섬 돌로르 시트 아멧, 컨설턴트 아디피싱 엘리트. Sed nec tortor at lectus tempus tempor. 서스펜디세 텔루스 디암, 피니버스 에우 딕텀 논, 베리에이션 및 입섬.
<br /><br />

#### 직조기 예제
* 사용 `source="loom"`
{% multi_lang_include video.html id="c1d3199463c448e8918f046265b54eb2" source="loom" %}

{% endtab %}
{% tab Markdown %}

{% raw %}
```html
{% multi_lang_include video.html id="[youte_id]" source="youtube" %}
```
{% endraw %}

오른쪽 또는 왼쪽으로 정렬하고 최대 너비를 50%로 제한하려면 `align` 매개변수 = `left` 또는 `right` 를 사용합니다:
{% raw %}
\`\`\`html
{% multi_lang_include video.html id="[ytube_id]" align="left" source="youtube" %}

{% multi_lang_include video.html id="[youe_id]" align="right" source="youtube" %}
\`\`\`
{% endraw %}

룸 예제:
{% raw %}
```html
{% multi_lang_include video.html id="[lid]" source="loom" %}
```
{% endraw %}

{% endtab %}
{% endtabs %}

#### 더 높은 해상도를 위한 상태 배치가 포함된 추천 동영상 레이아웃

고해상도 표시를 위해 왼쪽에 정적 동영상을 배치하는 추천 동영상 레이아웃을 사용하려면 페이지의 yaml 헤더에 `video_id` 및 `video_type` (예: `youtube`)을 추가합니다. 기본적으로 `video_source` 은 `youtube` 으로 설정되어 있습니다.

{% raw %}
```yaml
layout: featured_video
video_id: [video_id]
video_source: youtube
```
{% endraw %}

## 목록 테스트
{% tabs %}
{% tab Styling %}
#### Bullet

- 목록 1
  - 하위 목록 1
- 목록 2
  - 하위 목록 2a
    - 하위 목록 2
- 목록 3

#### 번호

1. 목록 1
   - 하위 목록 1
2. 목록 2
3. 목록 3
   - 하위 목록 3a
   - 하위 목록 3b
     - 하위 목록 3
4. 목록 4
    1. 하위 목록 4a
        1. 하위 목록 4
    2. 하위 목록 4b
        1. 하위 목록 4

{% endtab %}
{% tab Markdown %}
\`\`\`
#### Bullet

- 목록 1
  - 하위 목록 1
- 목록 2
  - 하위 목록 2a
    - 하위 목록 2
- 목록 3

#### 번호

1. 목록 1
   - 하위 목록 1
2. 목록 2
3. 목록 3
   - 하위 목록 3a
   - 하위 목록 3b
     - 하위 목록 3
4. 목록 4
    1. 하위 목록 4a
        1. 하위 목록 4
    2. 하위 목록 4b
        1. 하위 목록 4
\`\`\`
{% endtab %}
{% endtabs %}

## 접을 수 있는 콘텐츠 테스트
{% tabs %}
{% tab Styling %}
{% details Click me to Expand %}
#### 보세요! 숨겨진 코드 블록!

```python
print("hello world!")
```
{% enddetails %}
{% endtab %}
{% tab Markdown %}
{% raw %}
```liquid
{% details Click me to Expand %}
...
{% enddetails %}
```
{% endraw %}
{% endtab %}
{% endtabs %}

## 탭 테스트

#### 사용자 지정 탭

{% tabs local %}
{% tab OBJECTIVE-C %}

`AppDelegate.m` 파일에 다음 코드 줄을 추가합니다:

```objc
{% if include.platform == 'iOS' %}#import "Appboy-iOS-SDK/AppboyKit.h"{% else %}#import <AppboyTVOSKit/AppboyKit.h>{% endif %}
```

`AppDelegate.m` 파일 내에 `application:didFinishLaunchingWithOptions` 메서드에 다음 스니펫을 추가합니다:

```objc
[Appboy startWithApiKey:@"YOUR-API-KEY"
         inApplication:application
     withLaunchOptions:launchOptions];
```

{% endtab %}
{% tab swift %}

Braze SDK를 CocoaPods 또는 Carthage와 통합하는 경우 `AppDelegate.swift` 파일에 다음 코드 줄을 추가하세요:

```swift
{% if include.platform == 'iOS' %}#import Appboy_iOS_SDK{% else %}#import AppboyTVOSKit{% endif %}
```

Swift 프로젝트에서 Objective-C 코드를 사용하는 방법에 대한 자세한 내용은 [Apple 개발자 문서][apple\_initial\_setup\_19]를 참조하세요.

`AppDelegate.swift` 에서 `application(application: UIApplication, didFinishLaunchingWithOptions launchOptions: [NSObject: AnyObject]?) -> Bool` 에 다음 스니펫을 추가합니다:

```swift
Appboy.start(withApiKey: "YOUR-API-KEY", in:application, withLaunchOptions:launchOptions)
```
{% endtab %}
{% endtabs %}

#### 사용법
{% raw %}
**탭을** `{% tabs %}` 및 `{% endtabs %}`
개별 **탭을** Liquid 코드와 탭 이름으로 묶어 `{% tab [Tab name] %}` 및 `{% endtab %}`
{% endraw %}

{% alert important %}
 참고 페이지의 탭 수는 일정해야 하며, 그렇지 않으면 탭 콘텐츠가 숨겨질 수 있습니다.
 예를 들어 한 탭 세트에 `C++`,`C-Sharp` 및 `JS` 이 있고 다른 탭 세트에 `C-Sharp` 및 `JS` 이 있는 경우입니다,
`C++`를 클릭하면 다른 섹션은 아무것도 표시되지 않습니다. 해결 방법은 다음 로컬 탭 옵션을 참조하세요.
{% endalert %}

{% raw %}
```liquid
{% tabs %}
{% tab objective-c %}
Content of objective-c
{% endtab %}
{% tab swift %}
Content of swift
{% endtab %}
{% endtabs %}
```
{% endraw %}

#### 로컬 탭
특정 섹션의 탭 콘텐츠만 변경하는 탭과 같은 독립형 탭의 경우 상위 탭 블록에서 로컬 매개변수를 사용합니다.

{% raw %}
```liquid
{% tabs local %}
...
{% endtabs %}
```
{% endraw %}

#### 하위 탭
탭 내의 탭의 경우 `subtabs` 및 `subtab` 을 사용할 수 있습니다. 기본 설정은 `local` 입니다.
글로벌의 경우 `subtabs`, `global` 옵션을 사용합니다: {% raw %}`{% subtabs global %}`{% endraw %}

{% tabs local %}
{% tab Tab 1 %}
탭 콘텐츠 1
{% subtabs %}
{% subtab Subtab 1a %}
하위 탭 1a 콘텐츠
{% endsubtab %}
{% subtab Subtab 2a %}
하위 탭 2a 콘텐츠
{% endsubtab %}
{% endsubtabs %}
{% endtab %}
{% tab Tab 2 %}
탭 콘텐츠 2
{% subtabs %}
{% subtab Subtab 1b %}
하위 탭 1a 콘텐츠
{% endsubtab %}
{% subtab Subtab 2b %}
하위 탭 2a 콘텐츠
{% endsubtab %}
{% endsubtabs %}
{% endtab %}
{% endtabs %}

##### 마크다운
{% raw %}
```
{% tabs local %}
{% tab Tab 1 %}
tab content 1
{% subtabs %}
{% subtab Subtab 1a %}
Subtab 1a content
{% endsubtab %}
{% subtab Subtab 2a %}
Subtab 2a content
{% endsubtab %}
{% endsubtabs %}
{% endtab %}
{% tab Tab 2 %}
tab content 2
{% subtabs %}
{% subtab Subtab 1b %}
Subtab 1a content
{% endsubtab %}
{% subtab Subtab 2b %}
Subtab 2a content
{% endsubtab %}
{% endsubtabs %}
{% endtab %}
{% endtabs %}
```
{% endraw %}

[1]: {% image_buster /assets/img_archive/code_snippet.png %}
