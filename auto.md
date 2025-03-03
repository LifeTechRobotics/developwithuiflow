---
# Page settings
layout: default
keywords:
comments: false

# Hero section
title: 自律走行
description: お掃除ロボットのように、走行中に前方に障害物があった場合、方向変換するようにしてみます。

# Author box
# author:
#     title: About Author
#     title_url: '#'
#     external_url: true
#     description: Author description

# Micro navigation
micro_nav: true

# Page navigation
page_nav:
    prev:
        content: ラジコン操作
        url: /remote
    next:
        content: 今後について
        url: /future
---

障害物を自動で避けるよう
-------------------------
### センサーを追加する
UIFlow 1.0 を開きます。

左下の Units を選択し、➕ をクリックします。
*sonic* を入力し、検索します。
ULTRASONIC-I.O を選択し、OK ボタンをクリックします。
センサー unit が追加されます。

### センサーの動作をプログラミングする
5cm以内に障害物が検知された場合、右へ90度回転します。

計算式←Markdown mathが対応されていない？


### 実行してみる
スマホでQRコードを読み取り、ラジコンの操作画面が表示されます。

