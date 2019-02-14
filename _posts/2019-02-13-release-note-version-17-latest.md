---
layout: fix
title: "4D v17 修正リスト"
date: 2019-02-11 09:00:00
categories: 修正リスト
tags: "17.1" 
build: 233337
version: 17.x

---

**バージョン**: {{page.version}}  
**ビルド**: {{page.build}}  

* ACI0098939 Mac 64ビット版のみ。CEF版Webエリアは``WA Evaluate javascript``に実行が低速でした。システム版と比較しておよそ500倍の時間を要します。Webエリア上でマウスポインターを移動すると，幾らか速度が改善されますが，それでもかなり低速でした。

**注記**: 修正により，速度の問題は改善されましたが，それでもシステム版のほうが``div``の操作は高速です。

* ACI0098697 Mac 64ビット版のみ。エクスプローラーの「拡大」アイコンをクリックすると，ウィンドウが過剰にリサイズされ，復帰できなくなりました。

* ACI0099065 64ビット版のみ。``PRINT LABEL``で用紙またはラベルの枠外にオブジェクトが印刷されることがありました。