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

# 一つのサーボモータを動かす

## サンプルプログラムを動かしてみる
プロジェクトファイル： Servo_ATOMLite.m5f

実行方法は、**UIFlowの導入**ー**サンプルプログラムの動かし方** を参照。

### サンプルプログラムができること
左の車輪だけを動かします。

速度を上げながら正回転 > 停止 > 速度を上げながら逆回転 > 停止 の順で動きます。

## プログラミング手順
### サーボ Unit を追加する
UIFlow 1.0 を開きます。

左下の Units を選択し、➕ をクリックします。
*servo* を入力し、検索します。
SERVO を選択し、OK ボタンをクリックします。
サーボ unit (servo_0) が追加されます。
![1](../images/servo/1.png)

### Port を設定する
追加された servo unit をクリックし、利用する port を指定します。

基板によって違いますが、ここでは、Custom > SDA/TX を 19 に設定します。
![2](../images/servo/2.png)

### 速度を設定する
Units > SERVO をクリックし、サーボを回転させるため、**Set (0 ~ 180) degree turn** を使います。
ドラッグ＆ドロップしてプログラムを組みます。
![3](../images/servo/3.png)

- 速度の指定範囲    0 〜 180
    - 0     最大速度（逆回転）
    - 90    停止
    - 180   最大速度（正回転とする）
