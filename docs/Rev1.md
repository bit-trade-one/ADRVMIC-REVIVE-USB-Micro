[![BTO-logo](https://bit-trade-one.co.jp/wp/wp-content/uploads/2022/05/logo.png)](https://bit-trade-one.co.jp/)

通常版を使用する場合には  
通常版設定ツールと  
通常版ファームウェアが書き込まれたREVIVE-USB-Microが必要です  

REVIVE-USB-Micro-Rev1は販売時コチラのファームウェアが書き込み済みです。

## 目次
- [通常版ダウンロード](#通常版ダウンロード)  
- [設定ツール使用方法](#設定ツール使用方法)  
- [ファームウエア書き換え方法](#ファームウエア書き換え方法)  

---

# 通常版ダウンロード
### [通常版設定ツールダウンロードリンク](https://github.com/bit-trade-one/ADRVMICR2-REVIVE-USB-Micro-Rev2/raw/master/App/Rev1/Revive_Micro_CT.exe)
[過去バージョン一覧](https://github.com/bit-trade-one/ADRVMICR2-REVIVE-USB-Micro-Rev2/tree/master/App/Rev1)

ピンの割当などを行う設定ツールです。
本設定ツールはWindowsPCにて動作します。

### [通常版ファームウェアダウンロードリンク(v001)](https://github.com/bit-trade-one/ADRVMICR2-REVIVE-USB-Micro-Rev2/raw/master/Firmware/Rev1/REVIVE_MICRO_v001.zip)
[過去バージョン一覧](https://github.com/bit-trade-one/ADRVMICR2-REVIVE-USB-Micro-Rev2/blob/master/Firmware/Rev1/REVIVE_MICRO_v001.zip)  

ファームウェアはハードウェアの中に書き込まれているソフトウェアです。  
不具合修正や機能追加された新しいファームウェアが公開された際、   
ファームウェアをアップデートすることで新しい機能が使用できます。  

---


# 設定ツール使用方法
## 1. ダウンロード

上記のダウンロードリンクをクリックすると自動的にダウンロードされます。
![image](https://user-images.githubusercontent.com/85532743/174980131-56e51352-1579-4d77-95c0-025a3aa4913d.png)

PCの任意の場所にファイルをダウンロードして、起動してください。

## 2. 設定ツール使用方法

解凍したexeファイルを起動すると設定画面が開きます。
![image](https://user-images.githubusercontent.com/85532743/174980583-ea6dfaae-626b-4098-9e9e-e9c3d059f485.png)

REVIVE-USB-Microをつなぐと設定が行えるようになります。 
繋いでも有効にならない場合は間違えた設定ツールとファームウェアの組み合わせである可能性があります。 再度ご確認ください。  
![image](https://user-images.githubusercontent.com/85532743/174980554-d72d9647-8063-49d0-807e-00fc18d313f3.png)



## 3 プログラマブルキー割り当て

12個のキーそれぞれにマウス/キーボード/ジョイパッドの機能を割り当てることが出来ます。

画面左側よりスイッチ番号/デバイスタイプ/割当て を選択後、  
設定ボタンを押すとREVIVE-USB-Microに設定が書き込まれます。
![image](https://user-images.githubusercontent.com/85532743/174980845-6f180306-0706-410c-a7ed-319e6f9f9b55.png)


## 4 マウス

マウスは以下の割当てから選ぶ事が出来ます。


- ####  左クリック

- #### 右クリック  

- #### ホイールクリック

- #### 上移動／下移動／左移動／右移動 
   1～255の範囲で移動速度設定が可能です。

- #### ホイール上／ホイール下
   1～255の範囲で移動速度設定が可能です。  

- #### カーソル速度変更
   このボタンが押されている間のみ、カーソル速度がここでの設定値に変更されます。  

## 5 キーボード

テキストボックスに入力された文字を出力できます。  
Ctrl／Shift／Alt／Winのチェックボックスにチェックを入れるとテキストボックスのキーと同時入力が出来ます。 



例：テキストボックスに「Delキー」を入力し、[Ctrl]と[Alt]にチェックを入れ「設定」を押すと、  
CTRL + ALT + DELが入力できるようになります。

## 6 ジョイパッド

レバー上下左右／ボタン1～12の中からそのピンに対応させたい物を選んでチェックを入れます。  
チェックを入れたもの全てが反応する様になります。  


例：「ボタン１」と「ボタン３」にチェックを入れ設定した場合、「ボタン１／３」の同時入力が可能です。


---

# ファームウエア書き換え方法

ファームウェアはハードウェアの中に書き込まれているソフトウェアです。  
不具合修正や機能追加された新しいファームウェアが公開された際、  
ファームウェアをアップデートすることで新しい機能が使用できます。  

## 1.準備
- __HIDBootLoader.exeを任意の場所にダウンロードしてください。__  
 [HIDBootLoader.exeダウンロードリンク](https://github.com/bit-trade-one/ADRVMICR2-REVIVE-USB-Micro-Rev2/raw/master/Firmware/Tool/HIDBootLoader.exe)   
  こちらは、Microchipが公開しているライブラリ「MCHPFSUSB」の中にある物と同一です。  
  HIDBootLoader.exeは.NET framework 2.0を用いて作成されています。
  HIDBootLoader.exeがうまく起動しない場合、MicrosoftのHP等からダウンロードし、インストールする必要があります。
  “Microsoft .NET framework”等のキーワードで検索を行い入手してください。  

- __必要なファームウェアを任意の場所にダウンロードしてください。__  
  
## 2. ファームウェア書き込み
- __設定ツール右下、UpdateボタンよりBOOTモードにします。__  
![image](https://user-images.githubusercontent.com/85532743/174981162-b00eb6e4-f26f-4c3c-a2ea-da92614e68cf.png)

- __ファームウェアの書き換えウィンドウで「はい」を選択してください。本体がBOOTモードに入ります。__    
![image](https://user-images.githubusercontent.com/85532743/174981209-45d1906a-5d3f-4984-b0d4-076718c2c9b6.png)

- __先程ダウンロードしたHIDBootLoader.exeを立ち上げてください。__    
![image](https://user-images.githubusercontent.com/85532743/170158526-76b20a94-d8ee-4429-b6af-8e27f3d92fe6.png)  
デバイスが認識されると上図の様に「Device attached」と表示されます。  
初めてBOOTモードで接続した時には、自動的にPCにドライバがインストールされます。（約１分程時間かかります） 
   
 
- __「Open Hex File」を押し、書き込みたいファームウェア(Hexファイル)を選択します。__  
![image](https://user-images.githubusercontent.com/85532743/169975424-6d0913f8-7b8a-43fa-84dc-eec7b0a77bd0.png)  

- __「Program/Verify」を押すとファームウェアが書き込まれます。__  
![image](https://user-images.githubusercontent.com/85532743/169975956-b5d252c5-158b-45fe-b4ad-20486a0c2c2f.png)  

- __「Erase/Program/Verify Completed Successfully」とウィンドウに表示され、緑のインジケータが最大になれば完了です。__    
USBケーブルを抜差しして再起動すると、ファームウェアが適応されます。
![image](https://user-images.githubusercontent.com/85532743/169977504-b4b4a0e0-5e7d-43fa-a13c-f173bf783330.png)

以上でファームウェアアップデートは完了です。
