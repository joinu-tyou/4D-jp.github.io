---
layout: post
title: "Windows Server 電源プラン"
date: 2019-01-09 23:44:23
categories: セットアップ 
tags: windows server
version: 16.x
---

デスクトップ版のWindows 10には，電力を節約するための設定（電源とスリープの設定/追加の電源設定）が用意されており，デフォルトの電源プランは，「バランス」となっています。サーバー版のWindows 2008-2016もそうです。「バランス」電源プランが有効されている場合，4D Serverは最高でも30-50%ほどのパフォーマンスに抑えられます。5%程度まで低下することもあります。対照的に，プランを「高パフォーマンス」に設定すれば，CPUの能力を常に100%発揮することができ，バックアップに要する時間やシーケンシャルクエリの速度が明らかに向上します。

<i class="fa fa-external-link" aria-hidden="true"></i> [slow-performance-on-windows-server-when-using-the-balanced-power-plan](https://support.microsoft.com/ja-jp/help/2207548/slow-performance-on-windows-server-when-using-the-balanced-power-plan)

<i class="fa fa-external-link" aria-hidden="true"></i> [power-performance-tuning](https://docs.microsoft.com/ja-jp/windows-server/administration/performance-tuning/hardware/power/power-performance-tuning)

省電力設定が有効になると，CPUはクロック周波数が引き下げられ，ある程度の時間，ある程度のリクエストが続かない限り，ずっと低速モードで動作します。CPUだけでなく，USBポートやネットワークインタフェースも省エネルギーモードに切り替わったり，スリープ状態になることさえあるかもしれません。「バランス」のような省電力指向の電源プランでデータベースを運用することには，あまりメリットがないようです。
