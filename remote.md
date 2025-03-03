---
# Page settings
layout: default
keywords:
comments: false

# Hero section
title: ラジコン操作
description: ロボットを遠隔操作できるようにしてみます。

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
        content: ロボット動作
        url: /robot
    next:
        content: 自律走行
        url: /auto
---

遠隔でロボットを操作する
-------------------------
### コントローラー風の操作画面を作成する
UIFlow 1.0 を開きます。

Remote+ をクリックします。

前後左右 4 つのボタンを配置します。

真ん中に停止ボタンを配置します。丸いボタンにするため、Edges を Pill に設定します。

速度指定スライダーを配置します。
    - Min Value : 0
    - Max Value : 90

### 各ボタンの動作をプログラミングする




### 実行してみる
スマホでQRコードを読み取り、ラジコンの操作画面が表示されます。

