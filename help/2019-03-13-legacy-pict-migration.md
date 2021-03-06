---
layout: page
title: PICT形式のアイコン画像
permalink: /help/2019-03-13/
standalone: true
---

## ポイント

* v12以前にフォームウィザードで作成したフォームのアイコン画像は，4Dに収録されていた``cicn``または``PICT``リソースを参照している

* ``15000``以下の若いリソースIDは，4Dに収録されている画像のために予約されていた

* ``cicn``または``PICT``は，QuickDraw（``PICT``）形式なので，64ビット版では表示されない

* 標準コマンドの``CONVERT PICTURE``または``WRITE PICTURE FILE``で``PICT``を``png``あるいは``jpeg``に変換できるが，それには32ビット版の4Dが必要

* 表示されなくても，4Dに収録されていた``PICT``がどんな画像だったのかはIDから推測できる

* Resourcesフォルダー内の画像ファイルは，Finder/エクスプローラーまたは4Dのツールボックスからフォームエディターにドラッグ＆ドロップできる

**注記**: 下記の方法でPICT画像を復元できるとはいえ，当時のアイコン画像はシンプルなドット絵なので，この機会にもっとキレイな画像にすると良いでしょう。

## 動画

[![image](https://user-images.githubusercontent.com/10509075/54258061-c6933500-45a4-11e9-8521-ab5b82d0ce9a.jpg)](https://imgur.com/a/fSLuZvr "image")

[imgur.com](https://imgur.com/a/fSLuZvr)

## 手順

旧バージョンに収録されていた``cicn``および``PICT``リソースのPNG版をダウンロード

[cicn-PICT.zip](https://github.com/4D-JP/4D-jp.github.io/files/2959977/cicn-PICT.zip)

展開したファイル群をアプリケーションResourcesフォルダー（サブディレクトでもOK）に置く

<img width="770" alt="スクリーンショット 2019-03-13 15 12 55" src="https://user-images.githubusercontent.com/10509075/54257412-8fbc1f80-45a2-11e9-8b54-b5073cc365b3.png">

問題のあるフォームをエディターで開く

<img width="915" alt="スクリーンショット 2019-03-13 15 34 24" src="https://user-images.githubusercontent.com/10509075/54258278-7ff20a80-45a5-11e9-9a45-11058b85111a.png">

PICT画像のID（ピクチャライブラリ）

<img width="762" alt="スクリーンショット 2019-03-13 15 34 51" src="https://user-images.githubusercontent.com/10509075/54258310-91d3ad80-45a5-11e9-91ea-daf2b2be2e1e.png">

PICT画像のID（プロパティリスト）

<img width="310" alt="スクリーンショット 2019-03-13 15 35 37" src="https://user-images.githubusercontent.com/10509075/54258355-aadc5e80-45a5-11e9-99c6-63ad7ec85f3d.png">

対応するPNG画像を直接フォームエディター上のオブジェクト（ボタン・ピクチャボタン・ピクチャ等）にドラッグ＆ドロップする

<img width="915" alt="スクリーンショット 2019-03-13 15 37 00" src="https://user-images.githubusercontent.com/10509075/54258408-dd865700-45a5-11e9-8eb9-81d7c0ac2c46.png">
