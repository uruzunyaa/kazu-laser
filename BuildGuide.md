# Build Guide
こちらは自作キーボードキット kazu-laser のビルドガイドになります。

動画版もありますので、併せてご参照ください。

https://www.youtube.com/watch?v=zEUvSC2t4i8

## はじめに
この度は、「kazu-laser」をお買い上げいただきまして誠にありがとうございます。

この製品はPowerPoint等の資料発表用に作られた自作キーボードキットです。

ファームウェアについては、VIA Custom UI for Vial を用いてカスタマイズする事が出来ます。

本製品は組み立てが必要なキットです。

組立工程の中には、ハンダ付けや細いねじを締める工程があります。
あらかじめ必要な工具（後述）を用意した上で、組立を始めてください。

![kazu-laser](https://github.com/uruzunyaa/kazu-laser/blob/main/image/DoneBuild.jpg)

## Parts

### キット内容物

キット内容物は以下のようになっています。

| 部品名                 | 個数 | 詳細                                                   |
|:---------------------|:-----------|:----------------------------------------------------------|
| PCB(ミドルプレート)                  | 1   |                                                           |
| スイッチプレート             | 1   |                                                           |
| ボトムプレート         | 1  |                                               |
| スルーホールダイオード         | 10 | スイッチングダイオード1N4148       |
| レーザーモジュール         | 1 | IEC 68025-1　クラス2 |
| レーザーモジュール固定用ワイヤー         | 1 |                                            |
| DCDCコンバーター             | 1      |PFMステップアップDCDCコンバーター HT7733A |
| コンデンサ              | 1 |   シルミックⅡ アルミ電解コンデンサ 16V 22μF　RFS-16V220ME3#5    |
| インダクタ            | 1       | マイクロインダクター 100μH AL0510-101K |
| リセットスイッチ             | 1      | タクタイルスイッチ - 2pin 3.5x6x4.3mm |
| スライドスイッチ(主電源スイッチ)             | 1      | 垂直スライドスイッチ SS12D00G3 |
| スタビライザー 2U       | 1       | MX用2Uスタビライザー   |
| 電池ホルダー 単4 | 2       | BH-411-4P24 または寸法の一致する互換品 |
| 六角スペーサーM2 11mm         | 4       |                                                           |
| 六角スペーサーM2 6mm         | 2       |                                                           |
| M2小ネジ 3~4 mm          | 12以上| 予備を入れています。基本的に14個程度同封されています。 |

### 別途用意する物


| 部品名                 | 必要個数   |  主な購入先                          | 補足 |
|:---------------------|:--------|:----------------------------------|:-----------------------------------------------|
| BLE Micro Pro                  | 1   | https://shop.yushakobo.jp/products/ble-micro-pro    |                         |
| コンスルー     | 2   | https://shop.yushakobo.jp/products/31?variant=37665714438305 |**高さ2.5mm** の 12ピン or 13ピン         | 
| キースイッチ         |  5  | 遊舎工房等、お好みの物 |Cherry MX である事。(ロープロファイル不可)                                              | 
| キーキャップ         | 2U×1  1U×4  |  遊舎工房等、お好みの物  |  |
| 単四電池         | 2 | コンビニエンスストア等 | 1.5V制の一般的な単4電池である事。  |

### 必要な工具等
| 名前                 | 補足                                                   |
|:---------------------|:----------------------------------------------------------|
| はんだごて | はんだ付けを行うのに必要です。 |
| はんだ     | はんだ付けを行うのに必要です。|
| ニッパー    | 部品の足を切るのに使用します。                  |
| ＋ドライバ | ネジを止める際に使用します。 |
| （はんだ吸い取り線）   | はんだ付けを外す際に使用します。失敗しなければ必要ありませんが、用意をオススメします。  |


## 組み立て

### 初心者の方へ

レーザーモジュールを除き、取り付ける部品にはミドルプレートの付ける面に印が付いています。

基板のどちらの面にはんだ付けしたら良いか分からない時は、基板上に書かれた部品のマークを確認しましょう。

### ダイオードを取り付ける

まず、ダイオードの足を曲げ、5個取り付けます。

取り付ける場所は、裏面に書かれている D1 ~ D5 の場所です。

**ダイオードには向きがあり** 、黒く塗られた向きを示す線が入っています。

この線を、基板の四角のマークに合わせます。

![diode](https://github.com/uruzunyaa/kazu-laser/blob/main/image/diode.png)


はんだ付け出来たら、はみ出ている足をニッパーで切ります。

### レーザーモジュールを取り付ける

次に、レーザーモジュールを取り付けます。

場所は、D6 と書かれた場所です。

まず、導線のカバーを少しはがします。 赤と黒のカバーを、はんだ付け出来るように外します。

**この時、あまり長く切りすぎないようにしてください。** 失敗した時に、取り返しがつかなくなります。

手順は以下を参考にしてください。

1. ニッパー等を用いて中の導線を切らないよう、切れ込みを入れます。
1. 銅線の皮を抑えながら引っ張ってください。**※レーザー部分を抑えないでください。銅線が根本から外れます。**
1. カバーを剥くのに失敗したら、細かく切れ込みを入れながら同じ手順を繰り返しながら再チャレンジしましょう。
1. 成功したら、飛び出している足を切ります。

カバーを剥いたレーザーモジュール

![lasercut](https://github.com/uruzunyaa/kazu-laser/blob/main/image/lasercut.jpg)

カバーを外せたら、はんだ付けをします。**この部品にも向きがあります。**

赤の部分を**＋**、黒の部分を **ー**にはんだ付けします。


### レーザーモジュールを固定する

キットに同封されている銀のワイヤーを使用し、レーザーモジュールを固定します。

レーザーモジュールの溝に、2周程度硬く巻き付けます。レーザーモジュールが安定していたら、はんだ付けをして固定します。

残っているワイヤーを切ります。

画像は他の部品も付いていますが、レーザーモジュールが画像のような状態となっていれば成功です。

![laser](https://github.com/uruzunyaa/kazu-laser/blob/main/image/laser.jpg)

### リセットスイッチを取り付ける

![resetswitch](https://github.com/uruzunyaa/kazu-laser/blob/main/image/list/resetswitch.png)

リセットスイッチをはんだ付けします。この部品に向きはありません。

場所は D6 のすぐ下の W_Pus のように書かれた場所です。

### コンデンサを取り付ける

![condenser](https://github.com/uruzunyaa/kazu-laser/blob/main/image/list/condenser.png)

コンデンサを向きに注意しながら取り付け、横に倒します。※倒さずに付けると、後々付けるボトムプレートに衝突します。

場所は C1 です。

**コンデンサには向きがあります。** 足の長さが長い方を **＋** 短い方を **ー** です。

はんだ付けしたら、足を切ります。

### DCDCコンバーターを取り付ける

![DCDC](https://github.com/uruzunyaa/kazu-laser/blob/main/image/list/DCDC.png)

**この部品も向きに注意してください。**

丸みを帯びた部分を基板の丸に合わせて、向きを合わせます。

場所はC1のすぐ下にある、 LX VOUT GND と書かれた場所です。 

向きを合わせたら、コンデンサと同様に寝かせます。

はんだ付けし、足を切ります。

### インダクタを取り付ける

![inductor](https://github.com/uruzunyaa/kazu-laser/blob/main/image/list/inductor.png)

向きはありません。はんだ付けをして、足を切ります。

場所は L1 です。

### 途中確認
ここまで作業し、以下のような状態になっていれば大丈夫です。

![DCDC,indoctor,condenser](https://github.com/uruzunyaa/kazu-laser/blob/main/image/condenser%2CDCDC%2Cinductor.png)


### スライドスイッチを取り付ける

![resetswitch](https://github.com/uruzunyaa/kazu-laser/blob/main/image/list/resetswitch.png)

向きはありません。はんだ付けをして、足を切ります。

スライドスイッチは表側の ON OFF と書かれた場所です。


### スタビライザーを取り付ける

![stabilizer](https://github.com/uruzunyaa/kazu-laser/blob/main/image/list/stabilizer.png)

下にスタビライザーのワイヤーが来るよう、しっかりと押し込みます。ここで、横から浮いていないか確認します。

ここで浮いていると、キーの動作が悪くなります。

![donestabilizer](https://github.com/uruzunyaa/kazu-laser/blob/main/image/toritukestabilizer.png)

### キースイッチを取り付ける
まず、スイッチプレートに全てのキーをはめ込みます。

その後、PCBミドルプレートに取り付け、はんだ付けをします。

スイッチプレートにはめ込む時から、基板の穴を見て、向きに注意してください。

![switchplate](https://github.com/uruzunyaa/kazu-laser/blob/main/image/switchplate.png)

### 電池ホルダーを取り付ける
**電池ホルダーの向きに注意してください。** 左が**＋** 右が **－** です。

### BLE Micro proを取り付ける
コンスルーを画像のように、金の点の部分がBLE側になるような向きで差し込みます。

BLEへコンスルーの取り付けが出来たら、そのまま基盤にも差し込みましょう。

※12ピンのコンスルーを使っている方は、USBポート側に寄せて使ってください。

![BLE](https://github.com/uruzunyaa/kazu-laser/blob/main/image/BLE.jpg)

差し込んだら、BLE Micropro側のみはんだ付けします。 (はんだ付けしなくても動作しますが、BLEを外したくなった時、上手く外す事が出来ません。)

### 動作確認等
組み立ては後ネジを取り付ければ完了です。ネジを取り付ける前に、動作確認を行いましょう。

まず、電池を入れる前に、部品の向きを確認してください。

向きに注意が必要な部品は以下の4つです。

- ダイオード(黒い部分と四角が一致しているか)
- コンデンサ(塗装が白くなっている部分が **－** )
- DCDCコンバーター(丸みを帯びた部分が基板の外側を向いているか)
- レーザーモジュール(赤が **＋** 黒が **－** となっているか)
- 電池ホルダー(2つとも右側にバネが付いているか)

これらの部品の向きを間違えた状態で電源を入れてしまうと、部品の故障したり、**最悪の場合発火します。**

確認出来たら、電池を入れ、レーザーポインタが付くか確認します。

その後、ファームウェアを書き込み、ネジを閉めたら完成です。

## ファームウェアの書き込み
ここからはファームウェアの書き込みを行います。

### BLE Micro proの設定
まず、BLE Micropro本体を、kazu-laserであると認識させるための設定を行います。

BLEと有線接続をした状態で、以下サイトにアクセスしてください。

https://sekigon-gonnoc.github.io/BLE-Micro-Pro-WebConfigurator/

- ブートローダーのアップデート
Update Bootloaderのタブをクリックします。

ble_micro_pro_bootloader_1_3_2を選択し、アップデートを行います。

![Bootloader Update](https://github.com/uruzunyaa/kazu-laser/blob/main/image/Update%20Bootloader.png)
https://github.com/uruzunyaa/kazu-laser/blob/main/image/Update%20Bootloader.png

- アプリケーションアップデート
Update Applicationのタブへ移動します。

ble_micro_pro_vial_1_3_6を選択し、アップデートします。

![Application Update](https://github.com/uruzunyaa/kazu-laser/blob/main/image/Update%20Application.png)

- キーボードの設定
Edit configのタブへ移動します。
Select keyboardの中から、 ble_micro_pro を選択します。

![Keyboard Setting](https://github.com/uruzunyaa/kazu-laser/blob/main/image/Keyboard%20Setting.png)

- kazu-laserの設定を書き込む
以下のファイルをダウンロードし、BLEMicropro のストレージ直下にアップロードしてください。

https://github.com/uruzunyaa/kazu-laser/blob/main/kazu_laser_config.bin

アップロード完了後、USB接続を一度解除し、再度接続する事で、設定が完了します。

### キーマップの設定
キーマップの設定を行います。以下サイトにアクセスし、キーボードを選択し接続します。
https://sekigon-gonnoc.github.io/via-custom-ui-for-vial/

UP SETTING から以下のデフォルトキーマップをアップロードするか、Keymapをクリックし、手動で編集を行ってください。

デフォルトキーマップは以下のようになっています。
![Keymap](https://github.com/uruzunyaa/kazu-laser/blob/main/image/defalt%20keymap.png)

使用ソフトに合わせてご使用ください。

- Googleスライド用
https://github.com/uruzunyaa/kazu-laser/blob/main/kazu_laser-vial-setting-GoogleSlide.json

- PowerPoint用
https://github.com/uruzunyaa/kazu-laser/blob/main/kazu_laser-vial-setting-PowerPoint.json

- KeyNote用(Mac)
https://github.com/uruzunyaa/kazu-laser/blob/main/kazu_laser-vial-setting-KeyNote.json

### 動作確認
USB接続を解除し、ペアリングを行います。

電源をONにした状態にすると、PC側からBluetoothの欄にKazu-laserが出てくるはずです。

![Bluetooth](https://github.com/uruzunyaa/kazu-laser/blob/main/image/Bluetooth.png)

接続後、正常に動作するか確認してください。

ペアリング後からは、キーマップの編集が無線でも行えます。

### ネジの取り付け
動作確認が完了したら、ネジを取り付け、ボトムプレートを閉じましょう。

## 完成！！
組み立てお疲れ様でした！

ぜひ、発表等を行う際にご活用し、良き自作キーボードライフをお過ごしください！

![Bluetooth](https://github.com/uruzunyaa/kazu-laser/blob/main/image/DoneBuild2.jpg)
