---
# Page settings
layout: default
keywords:
comments: false

# Hero section
title: ロボット動作
description: ロボットを前後左右に動かしてみます。

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
        content: サーボモータ動作
        url: /servo
    next:
        content: ラジコン操作
        url: /remote
---

# ロボットを動かす

## サンプルプログラムを動かしてみる
プロジェクトファイル： Robot_ATOMLite.m5f

実行方法は、**UIFlowの導入**ー**サンプルプログラムの動かし方** を参照。

### サンプルプログラムができること
ロボットが 前進 > 後退 > 左旋回 > 右旋回 > 停止 の順で動きます。

## プログラミング手順
### サーボ Unit を 2 つ追加する
車輪が 2 つのため、サーボ Unit を 2 つ追加します。

サーボ Unit の追加方法は、**サーボモータ動作**ー**サーボ Unit を追加する** を参照。

### それぞれの Port を設定する
2 つのサーボ Unit が利用する Port それぞれを設定します。

左：servo_0　右：servo_1

![1](../images/robot/1.png)
![2](../images/robot/2.png)

Port の追加方法は、**サーボモータ動作**ー**Port を設定する** を参照。

### 前進させてみる
両輪を同じ固定速度にします。
```
value_left = 10
value_right = 10
```
前進させるため、左サーボを正回転に、右サーボを逆回転にします。

```
servo_0 Set (90 + value_left) degree turn
servo_1 Set (180 - (90 + value_right)) degree turn
```

### 後退させてみる
両輪を同じ固定速度にします。
```
value_left = 10
value_right = 10
```
後退させるため、左サーボを逆回転に、右サーボを正回転にします。

```
servo_0 Set (90 - value_left) degree turn
servo_1 Set (180 - (90 - value_right)) degree turn
```

### 左旋回させてみる
両輪を同じ固定速度にします。
```
value_left = 10
value_right = 10
```
左旋回させるため、左右のサーボ両方を逆回転にします。

```
servo_0 Set (90 - value_left) degree turn
servo_1 Set (90 - value_right) degree turn
```


### 右旋回させてみる
両輪を同じ固定速度にします。
```
value_left = 10
value_right = 10
```
右旋回させるため、左右のサーボ両方を正回転にします。

```
servo_0 Set (90 + value_left) degree turn
servo_1 Set (90 + value_right) degree turn
```

