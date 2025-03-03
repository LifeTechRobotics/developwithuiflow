---
# Page settings
layout: default
keywords:
comments: false

# Hero section
title: サーボモータ動作
description: サーボモータで車輪を動かしてみます。

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
        content: 構成要素
        url: /component
    next:
        content: ロボット動作
        url: /robot
---

一つのサーボモータを動かす
-------------------------
### サーボ Unit を追加する
UIFlow 1.0 を開きます。

左下の Units を選択し、➕ をクリックします。
*servo* を入力し、検索します。
SERVO を選択し、OK ボタンをクリックします。
サーボ unit が追加されます。

### Port を設定する
追加された servo unit をクリックし、利用する port を指定します。

port image貼り付け

### 速度を設定する
- 速度の指定範囲    0 〜 180
    - 0     最大速度（後回転）
    - 90    停止 
    - 180   最大速度（前回転）



