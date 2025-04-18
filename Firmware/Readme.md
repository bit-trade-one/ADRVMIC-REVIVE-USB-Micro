# ファイルリスト

 - REVIVE_MICRO_Ex_v100.zip(通常版)　※2021/12/03 ロータリーエンコーダ＆チャタリング防止対応版更新
 - REVIVE_MATRIX.zip(マトリックス版)
 - HIDBootLoader.exe(ファームウェア書込ツール)
 - iOS
   - REVIVE_MICRO_v001i.zip(iOS対応・通常版)
   - REVIVE_Micro_MATRIX_v002i.zip(iOS対応・マトリックス版)
   
**iOS版を使用する場合は、専用のPCツールが必要になります。**  
**iOS版はキーボードのみ対応となります。マウス・ジョイパッドについては設定は可能ですが動作しません。**  
**iOS版につきましては暫定対応となり、すべてのiOSバージョン/デバイスにおいて動作を保証するものではありません。**
   
# REVIVE USB MICROファームウェア

REVIVE USB MICROのファームウェアと、Microchip社の  
ファームウェア書込ツールを公開しています。 

## ファームウェア書込ツール（HIDBootLoader.exe）の使い方

### 1. このソフトで何が出来るのか

REVIVE USB MICROはMicrochip社のPICと言うマイコンを用いて作られています。  
通常、PICマイコンにソフトを書き込む為には「ライタ」と呼ばれる書き込み装置が必要です。  
（Microchip社が出しているPICkitや、秋月電子のキットであるAKI-PICプログラマーなどが有名です）  

このソフトを用いれば、特別なライタを必要とせず、USBから直接マイコンのソフトを書き換える事ができます。  
ただし、その為にはマイコンにBootLoaderと呼ばれる特別なソフトがあらかじめ書き込まれている必要があり、またUSB経由で書き込むソフトもBootLoaderに対応したものになっていなければなりません。  
あらかじめ書き込まれるBootLoader自体は、「ライタ」で書き込まなければなりません。  

REVIVE USB MICROに付属しているマイコンにはこのBootLoaderと言う特別なソフトがあらかじめ書かれています。よって、特別なライタをお持ちでなくてもUSB経由でソフトを書き込むことができます。  
また、GitHubで公開されているREVIVE USB MICRO用のソフトはこのBootLoaderでの書き込みに対応したソフトになっています。  

このBootLoaderを使うことで、USB経由で簡単にソフトを書き換えて、REVIVE USBのソフトを様々に書き換える事ができます。  

### 2. 準備

HIDBootLoader.exeをダウンロードします。  
[HIDBootLoader.exeダウンロードリンク](https://github.com/bit-trade-one/ADRVMIC-REVIVE-USB-Micro/raw/master/Firmware/HIDBootLoader.exe)
（これは、Microchipさんが公開しているライブラリ「MCHPFSUSB」の中にある物と同一です）  

このソフトは.NET framework 2.0を用いて作成されています。  
お手持ちのパソコンに.NET frameworkがインストールされていない場合、MicrosoftさんのHPからこれらをダウンロードし、インストールしておく必要があります。  
“Microsoft .NET framework”等のキーワードで検索すると出てきます。  

書き込みたいソフトもダウンロードしておきます。  

### 3. ソフトの書き込み

最初に、設定ツールからREVIVE USB MICROをBOOTモードにします。
![](http://bit-trade-one.co.jp/wp/wp-content/uploads/2019/06/01soft.jpg)
右下の「Update」ボタンをクリックしてください。
![](http://bit-trade-one.co.jp/wp/wp-content/uploads/2019/06/02update.jpg)
するとこのようにダイアログが表示されます。
OKをクリックすると、REVIVE USB MICROがBOOTモードになります。

HIDBootLoader.exeを立ち上げます。  

![](http://bit-trade-one.co.jp/wp/wp-content/uploads/2019/06/03HIDTool.png)  
デバイスが認識されると上図の様に「Device attached」と表示されます。  
初めてBOOTモードで接続した時には、自動的にPCにドライバがインストールされます。（約１分程時間かかります）  

「Open Hex File」を押します。  
書き込みたいHexファイルを選択します。  
![](http://bit-trade-one.co.jp/wp/wp-content/uploads/2019/06/04choose.png)  
「Program/Verify」を押します。  
ソフトが書き込まれます。  
![](http://bit-trade-one.co.jp/wp/wp-content/uploads/2019/06/05Program.png)  
USBケーブルを抜き差しすると、書き込んだソフトが起動します。  

### EX もしbootモード設定が上手くいかない・間違えてしまった場合には

![](https://bit-trade-one.co.jp/wp/wp-content/uploads/2022/02/aur_pin.png)  
画像の赤丸に囲まれている中央のピンといずれかのGNDピンを接続した状態で、USBケーブルをパソコンと接続することで強制的にBootモードへ移行できます。
