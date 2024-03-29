# ADRVMIC よくある質問

## USB接続の製品の場合には、下記の点についてお確かめください。

 - 使用しているケーブルがデータ通信可能であるか。
   - 電力供給のみのケーブルであることが多々ございます
 - ブートスイッチ等、ファームウェア書き込みモードになっていないか。
   - 説明書にブートスイッチについての記載がある製品が対象です
 - USBポートから十分な電力が供給されているか。
   - 念の為、PC本体のマザーボード側USBコネクタでお確かめください
 - 同時に接続している機器が干渉していないか。
   - できる限り最小構成での試行をお願い致します

----

## Q: 作成したデバイスは別のPCでも使用できますか

### A: 可能です。一度設定したボタンマッピングはデバイスに保存されるため他のPCに接続しても同様に動作します。

----

## Q: 設定ツールからボードが認識されません。

### A: 旧版REVIVE用の設定ツールを利用していないかご確認ください。
新REVIVE Microの設定ツールは[こちら](https://github.com/bit-trade-one/ADRVMIC-REVIVE-USB-Micro/tree/master/App)からダウンロードできます。

----

## Q: 設定ツールでUpdateボタンを押すとボードが認識されなくなった

### A:  Updateボタンをクリックしますと、REVIVEの動作はファームウェアアップデートモードに移行します。
この状態では通常の機能が使用できませんのでご注意下さい。  
通常動作に戻す場合は一度USBでの接続を取り外し、再度接続することで通常動作モードにてREVIVEが動作します。 

----

## Q: マトリックス配線で同時押しが正常に動作しない

### A: 単体での入力に問題が見られない場合、REVIVE自体は問題なく動作していると考えられます。 

スイッチ周辺の結線に短絡や断線がないか、また同時押し用ダイオードを入れている場合はその周辺に問題がないか、ご確認くださいませ。 

----

## Q: 何も接続していないピンを残して大丈夫でしょうか

### A: プルアップされているため特に設定などは必要ありません。絶縁のみ、お気を付けください。

----

## Q: 入力遅延はどれくらいでしょうか

### A: USBポーリングレート（データ送信の間隔）は1msとなります。

----

## Q: LED内蔵の照光式押ボタンを使用したい

### A: ボタンを押している間点灯する回路として、図のように接続してください。

![](https://bit-trade-one.co.jp/wp/wp-content/uploads/2020/09/signed-url-redirect.png)

なお、恐れ入りますが抵抗Rの値につきましてはスイッチの仕様に合わせた値を選定くださいませ。  
また、動作の保証は致しかねますことご了承ください。

----

## Q: 1回路のスイッチに対しREVIVEを二台使い、二重化したい。(同時に複数のデバイスへ入力を行いたい)

### A：リレー等を使用しそれぞれを絶縁してお使いください。
参考回路を掲載しますが、動作の保証は致しかねます。

![](https://raw.githubusercontent.com/bit-trade-one/ADRVMIC-REVIVE-USB-Micro/master/image/REVIVE%E4%BA%8C%E9%87%8D%E5%8C%96%E5%8F%82%E8%80%83%E5%9B%9E%E8%B7%AF.png)

----

## Q: マルチメディア機能の音量調節やスリープボタンなどに設定はできますか？  

### A: 出来ません。
基本的なキー+Ctrl,Shift,Alt,Winいずれかの同時押しは可能ですがそれ以外は不可能です。  

----
## Q: MACのCommand(⌘)、Option（⌥）キーを入力したいです。

### A: Windows用キーボードをMacで使うと、Windows(❖)キーがMacのCommand(⌘)キー、altキーがMacのOption（⌥）キーに対応します。
----

