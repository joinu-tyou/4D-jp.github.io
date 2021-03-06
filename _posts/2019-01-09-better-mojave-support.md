---
layout: post
title: "macOS Mojave"
date: 2019-01-09 11:35:00
categories: リリースノート
tags: 17r4 mac 17.1
version: 17r4

---

近日中にリリース予定の17.1および17r3（Mac版）は，Xcode 10.1およびmacOS 10.14 SDKがコンパイルに使用されています。これにより，macOS Mojaveでウィンドウリサイズ時に発生する『ちらつき』現象が解消されています。

加えて，まもなくベータ版が公開される17r4では，主要なフォームオブジェクトが従来の``HITheme``APIから``NSCell``に変更され，システム標準のダークモードに対応しています。

システム標準のAPIで作り替えられたのは，リストボックス・階層ポップアップメニュー・ポップアップドロップダウンリストおよびコンボボックス（標準サイズを超えるものを除く）・ボタン・ラジオボタン・チェックボックス・タブコントロール・スプリッター・ルーラー・進捗インジケーター（非同期とプログレスバーを除く）ウィンドウ背景色・テキスト入力全般・四角形の各フォームオブジェクトです。グループボックスとスタティックテキストについては，現時点で対応してません。

フォントカラーは「自動」に設定されている場合にのみ，システムのテーマを継承します。なお，テスト目的のため，macOS Mojaveでは，``caps lock``キーを有効にすることにより，新旧のAPIを切り替えることができるようになっています。

**注記**: 17r4をダークモードに対応させるためには，64ビット版アプリケーションパッケージ内の``Info.plist``ファイルで``NSRequiresAquaSystemAppearance``キーを``NO``に設定する必要があります。
