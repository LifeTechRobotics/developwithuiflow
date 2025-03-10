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

# 遠隔でロボットを操作する

## サンプルプログラムを動かしてみる
プロジェクトファイル： Remote_ATOMLite.m5f

実行方法は、**UIFlowの導入**ー**サンプルプログラムの動かし方** を参照してください。

### リモート操作してみる
初回の場合、UIFlow の Remote+ パネルを開き、右上の ▶ アイコンをクリックすると、遠隔操作用の QR コードが生成されます。

2回目以降は、▶ の左の QR コードマークをクリックすると表示されます。
![1](../images/remote/1.png)

スマートフォンで QR コードをスキャンして操作画面を開きます。

<img src="../images/remote/2.png" alt="2" width="50%" height="50%">

### サンプルプログラムができること
- 速度調整スライダー
- 前進　　↑
- 後退　　↓
- 左旋回　←
- 右旋回　→
- 停止　　○

速度を設定してから、前進／後退／左旋回／右旋回をタップしてロボットを動かします。

真ん中の停止ボタンをタップしてロボットを停止します。

## プログラミング手順
### コントローラー風の操作画面を作成する
UIFlow 1.0 を開きます。

Remote+ パネルを開きます。

前後左右 4 つのボタンを配置します。

真ん中に停止ボタンを配置します。丸いボタンにするため、Edges を Pill に設定します。

速度指定スライダーを配置します。
    - Min Value : 0
    - Max Value : 90

### ボタン動作をプログラミングする

#### 停止ボタン
左右のサーボを停止します。

停止前の速度を退避します。

#### 前進・後退・左旋回・右旋回ボタン

前章**ロボット動作**のプログラムに、停止して再開の場合、停止前の速度で設定します。