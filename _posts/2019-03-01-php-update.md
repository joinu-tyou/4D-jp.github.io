---
layout: post
title: "PHPのアップデート"
date: 2019-03-01 13:14:00
categories: リリースノート
tags: 17r5 php
---

17r5では，64ビット版PHPのバージョンが``5.4.11``から``7.3.1``にアップデートされました。PHPの更新に伴い，OpenSSL（``1.0.0d``から``1.1.1a``）などのライブラリもアップデートされています。また，``ftp`` はFTPSもサポートするようになりました。

**注記**: 設計上の理由により，アプリケーション本体とPHPは，それぞれ固有のOpenSSLライブラリを持っています。

モジュールでは，``readline`` 新たに追加され，``ereg`` ``COM & .NET`` が取り除かれています。なお，このバージョン以降，32ビット版の4Dはリリースされません。