---
layout: post
title: "標準アクションとオブジェクトメソッドの両方が設定されたタブコントロールの振る舞い"
date: 2019-01-30 22:23:01
categories: 仕様 
tags: 17.x
version: 17.x
---

タブコントロールオブジェクトは，フォームページの切り替えに適しているため，標準アクションの「ページ移動」がデフォルトで設定されています。フォームオブジェクトには，標準アクションとオブジェクトメソッドの両方が設定できますが，「ページ移動」アクションが設定されているタブコントロールの場合，``On Clicked``で``FORM GOTO PAGE``コマンドで指定したベージに移動することはできません。標準アクションは，オブジェクトメソッドの後に実行されるためです。

v16まで，一部のアクションはオブジェクトメソッドの前に実行され，他のアクションはオブジェクトメソッドの後に実行されるといった具合に振る舞いが一貫していませんでした。v17では，標準アクションは常にオブジェクトメソッドの後に実行されるよう，仕様が統一されています。