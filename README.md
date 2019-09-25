# USB CABLE CHECKER2 取扱説明書

## 機能紹介

本製品には下記の機能があります。

------

- USBケーブルのワイヤの結線状況のチェック

- タイプCプラグが持つ内蔵抵抗値の確認(PD用E Markerの有無)

- 電源線の抵抗値の確認

- プラグシェルの地絡確認

------

## 各部の説明



## 使用方法

- **プラグ変換アダプタの判定**

本製品の電源をONにしてから、A側のコネクタとB側のコネクタどちらかに変換アダプタを接続します。

タイプCプラグの変換コネクタでCCに接続された内蔵抵抗があればOLEDディスプレイに抵抗値が表示されます。

OTG機能があるアダプタなら「OTG ENABLE」と表示されます。

- **ケーブルの判定**

本製品の電源をONにしてから、A側のコネクタとB側のコネクタをUSBケーブルで繋ぎます。

ワイヤが結線されていれば「CONNECTION」の所に対応したLEDが点灯します。

- **OLEDディスプレイ表示部**

A側とB側に繋いだケーブルのVBUSとGNDの**両方**が結線されていれば、ディスプレイにVBUS線とGND線抵抗値の**合計**の抵抗値が表示されます。
  
プラグ内に抵抗を内蔵したタイプCプラグを接続すると、CCに接続されたプルアップ/プルダウン抵抗の値とそれに応じた接続機器に通知される最大許容電流値が表示されます。
  
10kプルダウン抵抗を検知した場合はMARKEDケーブルと判定します。

## 電池の交換方法

<img src="https://lh4.googleusercontent.com/73-uiDd_kTbdbabOrrpPLtvO4b3hMHSL4-iFW5v5Pc7ej-z6dSuNb1CDhtPvfjaD_lXa7f9pGcEUowNurw1lupkVanWQa0A8-hYJPqf5NBU_KbsPa_jXTBsU3-CLVJ5qEW8lHLRWJsxaYE4luA" alt="D:\DATA\Desktop\DSC04517 (1).JPG" style="zoom:25%;" />

起動時、OLEDディスプレイに「LOW BATTERY」と表示されたら電池の交換時期です。

上記画像のようにマイナス端子と電池の隙間にマイナスドライバーの先を滑り込ませるようにしてテコの原理を利用して外します。

その後、新しいCR2032バッテリーのプラス側を上にして装着します。

## OLEDディスプレイ表示の解説

### [抵抗値]

GND線とVBUS線合計の抵抗値です。

これにはUSBプラグ-コネクタ間接触抵抗が含まれます。単位はミリΩ、精度は±15％です。

測定限界値は1100mΩで、それ以上は「HIGH」と表示されます。  

### [UP10K/SOURCE 3.0A]

Cプラグ内にVBUS-CC間に接続された10kΩの抵抗器を持ちます。

USBデバイスにホストが3Aの電流供給能力があるものとして認識させます。

この抵抗値の抵抗をプラグ内に持つケーブルはUSB規格外です。

### [UP22K/SOURCE 1.5A]

Cプラグ内にVBUS-CC間に接続された22kΩの抵抗器を持ちます。

USBデバイスにホストが1.5Aの電流供給能力があるものとして認識させます。

この抵抗値の抵抗をプラグ内に持つケーブルはUSB規格外です。  

### [DOWN5.1K/SINK 0.5A] 

Cプラグ内にVBUS-CC間に接続された56kΩの抵抗器を持ちます。

USBデバイスにホストが0.5Aの電流供給能力があるものとして認識させます。

USB規格で許可されたコネクタ内蔵プルアップ抵抗はこの値のみです。

### [DOWN1K/E-MARKED]

Cプラグ内にGND-VCONN間に接続された1kΩの抵抗器を持ちます。

これにより接続先USB機器にEマーカーIC内蔵ケーブルということを通知します。  

### [DOWN5.1K/SINK 0.5A]

Cプラグ内にGND-CC間に接続された5.1kΩの抵抗器を持ちます。

これにより接続先USB機器は可能であればホストとして動作します。  

### [OTG　ENABLE]

抵抗器ではありませんが、Mini-B、Micro-BコネクタのGND-ID端子間がショートしていると点灯します。

これにより接続先USB機器は可能であればホストとして動作します。  

### [S-G　SHORT]

プラグシェルがGNDと導通している場合表示されます。

なお、タイプC-Cケーブルでは規格でGNDとシェルが接続されることが定められています。 

### [SHIELD CONNECT]

両端のシェルがGNDとは独立したワイヤで接続されいる場合「SHIELD CONNECT」と表示されます。

なお、通常レガシーUSBケーブルのシールド線は通常はどちらか片方のプラグにだけ接続され、プラグ間導通はありません。  

## ワイヤ接続確認LEDの解説

![img](https://llstock.s3-ap-northeast-1.amazonaws.com/uploads/photo/image/405311/middle_stockimage.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAI7P6SP7G3K7DHTNA%2F20190925%2Fap-northeast-1%2Fs3%2Faws4_request&X-Amz-Date=20190925T100729Z&X-Amz-Expires=600&X-Amz-SignedHeaders=host&X-Amz-Signature=841e264b7922fd3a68fbea8940ffacacd916b6cd5eddf572e42f966e542c786e)

### [3.2]　

USB3.2接続に用いられるワイヤ。差動線の名称はA側コネクタ側の端子名に準拠しています。  

### CC

TypeCケーブルにおいて主にホスト、デバイスの識別やUSB PD通信に使用されるワイヤ。

様々な機能を「使用できるかどうか」がこのワイヤを通してデバイス間でやり取りされる。  

### SBU

Side Band UseとしてUSBデータ通信以外のデータ（音声や映像等）をやり取りする際に使用するワイヤ。

主にオルタネートモードで利用される。  

### TX1/2 及び RX1/2

USB3.0以降での 通信を行うワイヤ。

USB3.0では2対のワイヤを使ったデータ通信（SuperSpeed /SS)を、

USB3.2以降では4対のワイヤを使ったデータ通信（SuperSpeed+ / SS+)を行う。  

### [2.0]

USB1.0~USB2.0接続に用いられるワイヤ。  

### D

USB2.0迄のデータ通信 （LowSpeed / Full Speed 及びHigh Speed）を行うために使われるワイヤ。  

### VBUS及びGND

電源管理の為に使用するワイヤ。

