---
layout: post
title: "サブフォームの切り替え"
date: 2019-03-27 15:46:00
categories: 仕様
tags: 17.x form 
---

v16では，リスト型のサブフォームダブルクリックすると，``FORM SET INPUT``で指定した入力フォームに切り替わりましたが，v17では常にデフォルトの入力フォームが使用され，``FORM SET INPUT``で指定したフォームは使用されません。これは仕様です。以前の振る舞いはバグであり，意図的な設計によるものではありませんでした。サブフォームの内容は，``OBJECT SET SUBFORM``で明示的に切り替えることができます。
