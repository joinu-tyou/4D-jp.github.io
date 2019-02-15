---
layout: post
title: "クライアント/サーバー版はバイナリデータが含まれるオブジェクト型がORDAで更新できない"
date: 2019-02-15 10:31:00
categories: 注意点 
tags: mac 17r4 orda writepro viewpro 17r5
version: 17r4
---

4D Remote, 4D for iOSなど，ネットワーク版のORDAは，RESTインタフェースに支えられています。標準的なJSONとしてエクスポートできるようなオブジェクトであれば，クライアント側のORDAアクセスで更新できますが，``[object picture]``・Write Proドキュメント・View Proドキュメントなどが属性に含まれるオブジェクトは，ORDAの``entity.save()``で保存することができません。これは仕様です。

```
C_OBJECT($e)
$e:=ds.Invoices.get(5)
$e.writeProDocument:=Form.writeProDocument
$status:=$e.save()
```

このコードをクライアント側で実行した場合，オブジェクト型フィールドのオブジェクト型属性であるWrite Proドキュメントは更新されず，エラーも返されないことに注意してください。

バイナリタイプのオブジェクト型属性の``entitiy.save()``は，17r5でサポートされる予定です。それまでは，クラシックコマンドの``SAVE RECORD``を使用する必要があります（ACI0099139）。