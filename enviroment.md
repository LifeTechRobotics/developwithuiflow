---
# Page settings
layout: default
keywords:
comments: false

# Hero section
title: UIFlowの導入
description: UIFlowを導入するための環境設定を行います。

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
    # prev:
    #     content: Previous page
    #     url: '#'
    next:
        content: 構成要素
        url: /component
---

利用環境
-------------------------
- Ubuntu 22.04
- Atom Lite
- UIFlow 1.0

導入手順
-------------------------
### M5Burnerのインストール
<https://docs.m5stack.com/ja/uiflow/m5burner/intro> にアクセスし、M5Burner をダウンロードします。（Ubuntu OSの場合、*M5Burner_Linux* を選択します。）

![1](../images/enviroment/1.png)

ダウンロードした zip ファイルを展開します。

現在ログインユーザーを dialout グループに追加した後、M5Burner を起動します。
```shell
sudo usermod -a -G dialout username
cd M5Burner-v3-beta-linux-x64
./M5Burner
```
右上のアカウントアイコンをクリックし、M5Stack Community アカウントでログインします。アカウントを持っていない場合、Register ボタンで新規登録を行います。

<div class="callout callout--danger">
    <p><strong>新規登録のメール認証で Page Not Found エラーが出た場合</strong></p>
    <p>URL欄に最後の”]”を消すと解消されます。</p>
</div>

### M5デバイスへファームウェアを書き込む
Atom Lite を USB で PC に接続します。

初めて接続する場合、[USB ドライバー](https://docs.m5stack.com/ja/uiflow/m5core/program)をインストールする必要かもしれません。

<!-- M5Stack Basic の場合、*CORE* を選択して、*UIFlow 1.0* をダウンロードします。 -->

Atom Liteの場合、*ATOM* を選択して、*UIFlow_Lite* をダウンロードします。
![2](../images/enviroment/2.png)

M5Burner 画面で Burn → Next をクリックし、ファームウェアを書き込みます。
![3](../images/enviroment/3.png)

Wi-Fiの *SSID* と *Password* を入力し、Next をクリックします。
![4](../images/enviroment/4.png)

<div class="callout callout--info">
    <p><strong>ネットワークは 4G を選択してください。</strong></p>
</div>

Burn successfully, click here to return をクリックし書き込み完了します。
![5](../images/enviroment/5.png)

<!-- M5Stack Basic の画面に下記の状態になったら、Wi-Fi と Cloud へ接続OKです。

<div class="callout callout--danger">
    <p><strong>✕または？マークが付いた場合</strong></p>
    <p>Configure から Wi-Fi 設定を確認してみてください。</p>
</div> -->

Configure > Load から UIFlow Configuration 画面から API KEY を確認できます。
![6](../images/enviroment/6.png)

<div class="callout callout--info">
    <p><strong>API KEY</strong></p>
    <p>デバイスへ接続する際、API KEY が必要のため、メモしておきましょう。</p>
</div>

### サンプルプログラムの動かし方
<https://flow.m5stack.com/> にアクセスし、UIFlow 1.0 を開きます。
右上のアカウントアイコンをクリックし、 M5Stack Community アカウントでログインします。
![11](../images/enviroment/11.png)


右上の Open アイコンをクリックし、サンプルプログラム(.m5fファイル)を選択します。
![8](../images/enviroment/8.png)

右上のメニュー > Setting をクリックし、Api Key を入力し、Device を ATOM を選択し、デバイスへ接続します。
![10](../images/enviroment/10.png)

右下の Run ボタンをクリックすると M5Stack へ書き込まず一回のみ実行されます。
