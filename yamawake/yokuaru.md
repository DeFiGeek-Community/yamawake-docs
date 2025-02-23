---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# よくある質問

<details>

<summary>オークションにNFTを出品することは出来ますか？</summary>

出来ません。ERC20規格のトークンのみ出品可能です。

</details>

<details>

<summary>複数のトークンでオークションを開催することは出来ますか？</summary>

複数のトークンを出品したり、複数のトークンで入札することは共に出来ません。

</details>

<details>

<summary>入札で使えるのはETHみですか？</summary>

はい。ERC20での入札対応はv2にて実装予定です。

</details>

<details>

<summary>オークションは成功したものの、割当トークンが０になってしまうこともありますか？</summary>

参加者の入札額が合計入札額に対して小さいと、割当トークンが０になる可能性はありますが、TemplateV1ではその可能性は極めて低いです。よって、参加者全員に幾らかのトークンが割り当てられます。

</details>

<details>

<summary>初期ユーザーリワードはBase上で請求可能ですか？</summary>

いいえ。Base上では請求ができない仕様となっております。

Baseで行われたオークションで発生した初期ユーザリワードは、

Ethereum上でのみ請求が可能です。

詳しくは[初期ユーザーリワードの請求方法のページ](../readme/yzriwdo/qing-qiu-fang-fa.md)をご覧ください。

</details>
