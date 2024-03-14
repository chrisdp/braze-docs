---
nav_title: スタイリングの例
article: Styling examples
description: "ヘッダー、タブ、コードブロックなど、Blaze Docs上でページのスタイルを設定する方法です。"
page_order: 8 
noindex: true
---

# スタイリング例

ヘッダー、タブ、コードブロックなど、Blaze Docs上でページのスタイルを設定する方法です。

## ヘッダーテスト

{% tabs %}
{% tab Styling %}

# H1バナー
H1テキスト

Lorem ipsum dolor sit amet, consectetur adipiscing elit.Sed nec tortor at lectus tempus tempor.Suspendisse tellus diam, finibus eu dictum non, varius et ipsum.

## H2バナー
H2テキスト

Lorem ipsum dolor sit amet, consectetur adipiscing elit.Sed nec tortor at lectus tempus tempor.Suspendisse tellus diam, finibus eu dictum non, varius et ipsum.

### H3バナー
H3テキスト

Lorem ipsum dolor sit amet, consectetur adipiscing elit.Sed nec tortor at lectus tempus tempor.Suspendisse tellus diam, finibus eu dictum non, varius et ipsum.

#### H4バナー
H4テキスト

Lorem ipsum dolor sit amet, consectetur adipiscing elit.Sed nec tortor at lectus tempus tempor.Suspendisse tellus diam, finibus eu dictum non, varius et ipsum.

##### H5バナー
H5テキスト

Lorem ipsum dolor sit amet, consectetur adipiscing elit.Sed nec tortor at lectus tempus tempor.Suspendisse tellus diam, finibus eu dictum non, varius et ipsum.

###### H6バナー
H6テキスト

Lorem ipsum dolor sit amet, consectetur adipiscing elit.Sed nec tortor at lectus tempus tempor.Suspendisse tellus diam, finibus eu dictum non, varius et ipsum.

{% endtab %}
{% tab Markdown %}

\`\`\`
# H1バナー

## H2バナー

### H3バナー

#### H4バナー

##### H5バナー

###### H6バナー
\`\`\`
{% endtab %}
{% endtabs %}

## カスタムヘッダーアンカー

見出しにアンカーを追加するには、見出しがある行の末尾に次のコードを追加します。`anchor-text`をこの見出しのアンカーに置き換えます。小文字を使用し、単語と単語の間にハイフンを入れます。

\`\`\`
# 見出しテキスト{#anchor-text}
\`\`\`

番号記号`#`の後にカスタムアンカーが続く標準リンクを作成することで、カスタムアンカーを持つ見出しにリンクできます。

{% raw %}
```
Here is my [link](#anchor-text)
```
{% endraw %}

## フォントテスト

{% tabs %}
{% tab Styling %}

通常のテキスト

*テキストを強調する*

**太字**

_**太字強調**_

~~取り消し線~~

{% endtab %}
{% tab Markdown %}
\`\`\`
通常のテキスト

*テキストを強調する*

**太字**

_**太字強調**_

~~取り消し線~~
\`\`\`
{% endtab %}
{% endtabs %}

## 見積もりテスト

{% tabs %}
{% tab Styling %}
> 引用テキスト

#### インラインクォート
Lorem ipsum dolor ``sit amet, consectetur adipiscing elit``.Sed nec tortor at lectus tempus tempor.

#### 見積もりチャンク
```
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nec tortor at lectus tempus tempor.
```
{% endtab %}
{% tab Markdown %}
\`\`\`
> 引用テキスト

Lorem ipsum dolor ``sit amet, consectetur adipiscing elit``.Sed nec tortor at lectus tempus tempor.

``` Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nec tortor at lectus tempus tempor. ```
\`\`\`
{% endtab %}
{% endtabs %}

## テーブルテスト

{% tabs %}
{% tab Styling %}
インスタンス|ダッシュボードURL|RESTエンドポイント
----------- |---------------- | --------------------
US-01 | `https://dashboard.braze.com`または<br> `https://dashboard-01.braze.com` | `https://rest.iad-01.braze.com`
US-02 | `https://dashboard-02.braze.com` | `https://rest.iad-02.braze.com`
US-03 | `https://dashboard-03.braze.com` | `https://rest.iad-03.braze.com`
US-04 | `https://dashboard-04.braze.com` | `https://rest.iad-04.braze.com`
US-05 | `https://dashboard-05.braze.com` | `https://rest.iad-05.braze.com`
US-06 | `https://dashboard-06.braze.com` | `https://rest.iad-06.braze.com`
US-07 | `https://dashboard-07.braze.com` | `https://rest.iad-07.braze.com`
US-08 | `https://dashboard-08.braze.com` | `https://rest.iad-08.braze.com`
EU-01 | `https://dashboard.braze.eu`または<br> `https://dashboard-01.braze.eu` | `https://rest.fra-01.braze.eu`
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

#### 表の改行を列単位でリセットする
ワードブレークを既定のスタイルにリセットする必要がある表の列の場合、Markdownオプションを使用して、列に対応する`#`を4までとし、`.reset-td-br-1`、`.reset-td-br-2`、`.reset-td-br-3`、`.reset-td-br-4`を使用して表にクラスを追加します。

#### 使い方
\`\`\`
|イベント名|フィードの種類|説明|カスタム属性
| ------------------------------------ | ---------------------- | ----------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
|アンブロークンワードTHATISVERYLONGUNBROKENWORDTHATISVERYLONG|アンバウンドフィード|ユーザーのメールサーバーに電子メールが正常に配信されました。|`campaign_id`、`canvas_step_id`、`canvas_id`、`canvas_variation_id`|
|`UNBROKENHIGHLIGHTTHATISVERYLONGUNBROKENHIGHLIGHTTHATISVERYLONG`|未バインドフィード|ユーザーがメールを開きました。|`campaign_id`、`canvas_step_id`、`canvas_id`、`canvas_variation_id`|
|アプリ内メッセージインプレッション|プラットフォーム別フィード|ユーザーがアプリ内メッセージを表示しました。|`app_id`、`campaign_id`、`canvas_step_id`、`canvas_id`、`canvas_variation_id`|
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

\`\`\`
{% tabs local %}
{% tab Before %}

|イベント名|フィードの種類|説明|カスタム属性|
|------------------------------------------------------------------|------------------------|--------------------------------------------------------------|-------------------------------------------------------------------------------|
|アンブロークンワードTHATISVERYLONGUNBROKENWORDTHATISVERYLONG|アンバウンドフィード|ユーザーのメールサーバーに電子メールが正常に配信されました。|`campaign_id`、`canvas_step_id`、`canvas_id`、`canvas_variation_id`|
|`UNBROKENHIGHLIGHTTHATISVERYLONGUNBROKENHIGHLIGHTTHATISVERYLONG`|未バインドフィード|ユーザーがメールを開きました。|`campaign_id`、`canvas_step_id`、`canvas_id`、`canvas_variation_id`|
|アプリ内メッセージインプレッション|プラットフォーム別フィード|ユーザーがアプリ内メッセージを表示しました。|`app_id`、`campaign_id`、`canvas_step_id`、`canvas_id`、`canvas_variation_id`|

{% endtab %}
{% tab After %}

|イベント名|フィードの種類|説明|カスタム属性|
|------------------------------------------------------------------|------------------------|--------------------------------------------------------------|-------------------------------------------------------------------------------|
|アンブロークンワードTHATISVERYLONGUNBROKENWORDTHATISVERYLONG|アンバウンドフィード|ユーザーのメールサーバーに電子メールが正常に配信されました。|`campaign_id`、`canvas_step_id`、`canvas_id`、`canvas_variation_id`|
|`UNBROKENHIGHLIGHTTHATISVERYLONGUNBROKENHIGHLIGHTTHATISVERYLONG`|未バインドフィード|ユーザーがメールを開きました。|`campaign_id`、`canvas_step_id`、`canvas_id`、`canvas_variation_id`|
|アプリ内メッセージインプレッション|プラットフォーム別フィード|ユーザーがアプリ内メッセージを表示しました。|`app_id`、`campaign_id`、`canvas_step_id`、`canvas_id`、`canvas_variation_id`|
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}
{% endtab %}
{% endtabs %}

## リンクテスト
{% tabs %}
{% tab Styling %}
リンクはこちら:[Braze.com](https://www.braze.com){: height="36px" width="36px"}
{% endtab %}
{% tab Markdown %}
```
[Braze.com](https://www.braze.com)
```
{% endtab %}
{% endtabs %}

## イメージテスト
{% tabs %}
{% tab Styling %}
【画像】![Logo]({% image_buster /assets/img/braze-logo-mark.png %}){: style="max-width:30%;"}

#### Linked Image Test

リンク先の画像：[![Braze]({% image_buster /assets/img/braze-logo-mark.png %}){: style="max-width:30%;"}](https://www.braze.com)

#### 画像スタイル

![Text]({% image_buster /assets/img/logo-braze-fa.svg %}){: style="max-width:30%; color: green" }

#### 画像をアンカーする

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

## ギャラリーテスト
{% tabs %}
{% tab Styling %}
{% gallery %}
{{site.baseurl}}/assets/img_archive/EBTH_Email.png?bf892368baf287cba5ab9a6e3b09431d <br> これは[リンク](https://www.braze.com)です
{{site.baseurl}}/assets/img_archive/iHeartRadio_Email.png?ecd2c8fe148939b7de957fe85cd6317e <br> これも`comment`です
{{site.baseurl}}/assets/img_archive/Saucey_Email.png?b9768937a1cc12d4c08e55a52e700d68 <br> これもまた別の**コメント**です。
{{site.baseurl}}/assets/img/schellman_iso27001_seal_grey_CMYK_300dpi_jpg.png?1b1fb9dbb80b0332c62512dcf9c83258 <br> **画像タイトル**<br> 改行されるかどうかのテストです。
{{site.baseurl}}/assets/img/SOC2.png?6338040be8e98c4c9abe1f35b3e43e3a <br> これは通常のコメントです。
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

## インタラクティブな画像テスト
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

## コードスニペットテスト

{% tabs %}
{% tab Styling %}
#### コードテストの目的C
```objc
- (void)submitFeedback:(ABKFeedback * )feedback
 withCompletionHandler:(nullable void (^)(ABKFeedbackSentResult feedbackSentResult))completionHandler;
```

#### コードテストSwift
```swift
Appboy.sharedInstance()?.submitFeedback(feedback) { (feedbackSentResult) in
      print("Feedback sent: (feedbackSentResult)")
    }
```

#### コードテストJava
```java
@Override
public void onResume() {
  super.onResume();
  // Registers the BrazeInAppMessageManager for the current Activity. This Activity will now listen for
  // in-app messages from Braze.
  BrazeInAppMessageManager.getInstance().registerInAppMessageManager(activity);
}
```

#### コードテストjson
```json
{
   "attributes" : "Attributes" ,
   "events" : ["Array", "Of", "Object"],
   "purchases" : ["Array" ,"Of" ,"Purchase" ,"Object"]
}
```

#### コードテストJavaScript
```javascript
braze.subscribeToFeedUpdates(function(feed) {
  var cards = feed.cards;
  braze.showFeed(undefined, cards);
});
braze.requestFeedRefresh();
```

#### 色素検査
\`\`パイソン
\#!/usr/bin/python3

エンジンのインポートからランフォレストラン

「構文強調表示のテストコード!」

class Foo:
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

## アラートテスト

{% tabs %}
{% tab Styling %}

{% alert tip %}これはヒントです{% endalert %}

{% alert note %}これはメモです{% endalert %}

{% alert important %}これは重要な警告です{% endalert %}

{% alert warning %}これは警告です{% endalert %}

{% alert update %}これはアップデートです{% endalert %}

{% endtab %}
{% tab Markdown %}
{% raw %}
\`\`\`
{% alert tip %}
これはヒントです
{% endalert %}

{% alert note %}
これはメモです
{% endalert %}

{% alert important %}
これは重要な警告です
{% endalert %}

{% alert warning %}
これは警告です
{% endalert %}

{% alert update %}
これはアップデートです
{% endalert %}
\`\`\`
{% endraw %}
{% endtab %}
{% endtabs %}

## 組み込みビデオテスト
{% tabs %}
{% tab Styling %}
#### 埋め込み動画/YouTube
デフォルトはYouTube埋め込み。
{% multi_lang_include video.html id="XY5vFY" source="youtube" %}

#### 埋め込みビデオ右寄せ
{% multi_lang_include video.html id="XYuXoKIvFY" align="right" source="youtube" %}

Lorem ipsum dolor sit amet, consectetur adipiscing elit.Sed nec tortor at lectus tempus tempor.Suspendisse tellus diam, finibus eu dictum non, varius et ipsum.Lorem ipsum dolor sit amet, consectetur adipiscing elit.Sed nec tortor at lectus tempus tempor.Suspendisse tellus diam, finibus eu dictum non, varius et ipsum.Lorem ipsum dolor sit amet, consectetur adipiscing elit.Sed nec tortor at lectus tempus tempor.Suspendisse tellus diam, finibus eu dictum non, varius et ipsum.

#### 埋め込みビデオの左寄せ
{% multi_lang_include video.html id="XY5uXvFY" align="left" source="youtube" %}

Lorem ipsum dolor sit amet, consectetur adipiscing elit.Sed nec tortor at lectus tempus tempor.Suspendisse tellus diam, finibus eu dictum non, varius et ipsum.Lorem ipsum dolor sit amet, consectetur adipiscing elit.Sed nec tortor at lectus tempus tempor.Suspendisse tellus diam, finibus eu dictum non, varius et ipsum.Lorem ipsum dolor sit amet, consectetur adipiscing elit.Sed nec tortor at lectus tempus tempor.Suspendisse tellus diam, finibus eu dictum non, varius et ipsum.
<br /><br />

#### 織機の例
* use `source="loom"`
{% multi_lang_include video.html id="c1d3199463c448e8918f046265b54eb2" source="loom" %}

{% endtab %}
{% tab Markdown %}

{% raw %}
```html
{% multi_lang_include video.html id="[youte_id]" source="youtube" %}
```
{% endraw %}

右揃えまたは左揃えにし、最大幅を50%に制限するには、`align`パラメータ=`left`または`right`を使用します。
{% raw %}
\`\`html
{% multi_lang_include video.html id="[ytube_id]" align="left" source="youtube" %}

{% multi_lang_include video.html id="[youe_id]" align="right" source="youtube" %}
\`\`\`
{% endraw %}

織機の例：
{% raw %}
```html
{% multi_lang_include video.html id="[lid]" source="loom" %}
```
{% endraw %}

{% endtab %}
{% endtabs %}

#### 高解像度のためのステータス配置を備えた注目のビデオレイアウト

左側に静的な動画を配置して高解像度に表示するアイキャッチ動画レイアウトを使用するには、ページのyamlヘッダーに`video_id`と`video_type`（`youtube`など）を追加します。デフォルトでは、`video_source`は`youtube`に設定されています。

{% raw %}
```yaml
layout: featured_video
video_id: [video_id]
video_source: youtube
```
{% endraw %}

## リストテスト
{% tabs %}
{% tab Styling %}
#### 箇条書き

- リスト1
  - サブリスト1
- リスト2
  - Sub List 2a
    - Sub Sub List 2
- リスト3

#### 番号付き

1. リスト1
   - サブリスト1
2. リスト2
3. リスト3
   - Sub List 3a
   - Sub List 3b
     - Sub Sub List 3
4. リスト4
    1. Sub list 4a
        1. Sub Sub List 4
    2. Sub list 4b
        1. sub sub list 4

{% endtab %}
{% tab Markdown %}
\`\`\`
#### 箇条書き

- リスト1
  - サブリスト1
- リスト2
  - Sub List 2a
    - Sub Sub List 2
- リスト3

#### 番号付き

1. リスト1
   - サブリスト1
2. リスト2
3. リスト3
   - Sub List 3a
   - Sub List 3b
     - Sub Sub List 3
4. リスト4
    1. Sub list 4a
        1. Sub Sub List 4
    2. Sub list 4b
        1. sub sub list 4
\`\`\`
{% endtab %}
{% endtabs %}

## Collapsible Content Test
{% tabs %}
{% tab Styling %}
{% details Click me to Expand %}
#### 見て!A Hidden Code Block!

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

## タブテスト

#### カスタムタブ

{% tabs local %}
{% tab OBJECTIVE-C %}

`AppDelegate.m`ファイルに次のコード行を追加します。

```objc
{% if include.platform == 'iOS' %}#import "Appboy-iOS-SDK/AppboyKit.h"{% else %}#import <AppboyTVOSKit/AppboyKit.h>{% endif %}
```

`AppDelegate.m`ファイル内に、`application:didFinishLaunchingWithOptions`メソッド内に次のスニペットを追加します。

```objc
[Appboy startWithApiKey:@"YOUR-API-KEY"
         inApplication:application
     withLaunchOptions:launchOptions];
```

{% endtab %}
{% tab swift %}

Braze SDKをCocoaPodsまたはCarthageと統合する場合は、`AppDelegate.swift`ファイルに次のコード行を追加します。

```swift
{% if include.platform == 'iOS' %}#import Appboy_iOS_SDK{% else %}#import AppboyTVOSKit{% endif %}
```

SwiftプロジェクトでのObjective-Cコードの使用の詳細については 、 [ Apple Developer Docs][apple\_initial\_setup\_19]を参照してください。

`AppDelegate.swift`、次のスニペットを`application(application: UIApplication, didFinishLaunchingWithOptions launchOptions: [NSObject: AnyObject]?) -> Bool`に追加します。

```swift
Appboy.start(withApiKey: "YOUR-API-KEY", in:application, withLaunchOptions:launchOptions)
```
{% endtab %}
{% endtabs %}

#### 使い方
{% raw %}
**タブ**を`{% tabs %}`と`{% endtabs %}`で囲む
個々の**タブ**をリキッドコードで囲み、タブ`{% tab [Tab name] %}`と`{% endtab %}`の名前を
{% endraw %}

{% alert important %}
 ページ上のタブ数は統一してください。統一しないとタブの内容が隠れてしまう可能性があります。
 たとえば、あるタブセットに`C++`、`C-Sharp`および`JS`があり、別のタブセットに`C-Sharp`および`JS`がある場合、
では、誰かが`C++`をクリックしても、他のセクションは何も表示されません。回避策については、次のローカルタブオプションを参照してください。
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

#### ローカルタブ
特定のセクションのタブ内容のみを変更するタブなど、独立したタブの場合は、親タブブロックで local パラメータを使用します。

{% raw %}
```liquid
{% tabs local %}
...
{% endtabs %}
```
{% endraw %}

#### サブタブ
タブ内のタブの場合は、`subtabs`と`subtab`を使用できます。デフォルト設定は`local`です。
グローバル`subtabs`の場合は、`global`オプションを使用します。{% raw %}`{% subtabs global %}`{% endraw %}

{% tabs local %}
{% tab Tab 1 %}
タブの内容1
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
タブの内容2
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

##### Markdown
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
