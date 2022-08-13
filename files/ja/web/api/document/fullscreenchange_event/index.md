---
title: 'Document: fullscreenchange イベント'
slug: Web/API/Document/fullscreenchange_event
tags:
  - API
  - Fullscreen API
  - Reference
  - events
  - fullscreen
  - fullscreenchange
  - イベント
  - 全画面モード
translation_of: Web/API/Document/fullscreenchange_event
---
{{APIRef}}

`fullscreenchange` イベントは、ブラウザーが全画面モードに移行したり終了したりした直後に発生します。

| バブリング                   | あり                                                                                 |
| ---------------------------- | ------------------------------------------------------------------------------------ |
| キャンセル                   | 不可                                                                                 |
| インターフェイス             | {{domxref("Event")}}                                                         |
| イベントハンドラープロパティ | {{domxref("Document.onfullscreenchange", "onfullscreenchange")}} |

このイベントは、全画面モードに移行または終了しようとしている `Element` に送られ、それから `Document` までバブリングします。

\<p\<code>Element が全画面モードに移行しようとしているのか、終了しようとしているのかを判別するには、 {{domxref("DocumentOrShadowRoot/fullscreenElement", "DocumentOrShadowRoot.fullscreenElement")}} の値をチェックしてください。この値が `null` ならば、要素が全画面モードを終了しようとしており、そうでなければ全画面モードに移行しようとしています。

## 例

この例では、 `fullscreenchange` イベントのハンドラーが {{domxref("Document")}} に追加されます。

```js
document.addEventListener('fullscreenchange', (event) => {
  // document.fullscreenElement は、全画面モードにある要素があれば
  // それを指します。要素がなければ、このプロパティの値は null に
  // あります。
  if (document.fullscreenElement) {
    console.log(`Element: ${document.fullscreenElement.id} entered full-screen mode.`);
  } else {
    console.log('Leaving full-screen mode.');
  }
});
```

その他の例については [Element: fullscreenchange イベント](/ja/docs/Web/API/Element/fullscreenchange_event)を参照してください。

## 仕様書

| 仕様書                               | 状態                             |
| ------------------------------------ | -------------------------------- |
| {{SpecName("Fullscreen")}} | {{Spec2("Fullscreen")}} |

## ブラウザーの互換性

{{Compat("api.Document.fullscreenchange_event")}}

## 関連情報

- {{domxref("Document/fullscreenerror_event", "fullscreenerror")}}
- {{domxref("Element")}}: {{domxref("Element/fullscreenchange_event", "fullscreenchange")}} イベント
- [Fullscreen API](/ja/docs/Web/API/Fullscreen_API)
- [Fullscreen API のガイド](/ja/docs/Web/API/Fullscreen_API/Guide)