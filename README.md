# __chapter4 デジタルデータの表し方__
## 補助単位

__bit__...デジタルデータの最小単位

__byte__...8bitをまあとめた単位

## 文字の表現方法

__文字コード__...文字に数値を割り当てた物

### 文字コードの種類

 - ASCII
 - EBCDIC
 - シフトJISコード
 - EUC
 - Unicode

## 画像などの表し方

__画像や音声を数値に変換している__
> [!NOTE]
> ### 画像のbit数を求める
> 縦　×　横　×　色（2,4,8,16,24bit） = bit数

### 音声データの表し方

>__PCM方式を用いている__
>
>### 1.標本化...デジタルデータに変える（横軸）
>
>__サンプリング周期__..サンプリング（標本化）するときの、間隔を表している

>### 2.量子化...音を分ける（縦軸）
>
>__量子化ビット数__...量子化するときの間隔を表している
>
##  アナログデータのセンシングと制御技術

__センサ__...自然界のアナログデータを読み込む

__アクチュエータ__...電気信号を受け取って動く

### 制御方法
>
>__1.シーケンス制御__...決められた手順にそって動く
>
>__2.フィードバック制御__...定期的に測定し、目標値に近づける

# chapter5 CPUとコンピューターの5大装置

## 5大装置
>### (中央処理装置)
>- ### 制御装置　｝
>- ### 演算装置　｝
>- ### 記憶装置
>  主記憶装置
>　補助記憶装置
>- ### 入力装置
>- ### 出力装置

## ノイマン型コンピュータ

__プログラム内蔵方式__...実行時に主記憶装置にプログラムを読み込んでおく装置

__逐次制御方式__...命令を1づつ取り出して実行する方式

__アドレス__...主記憶装置でどこに何があるかを把握するためにある区画

## CPUの実行手順とレジスタ

__レジスタ__...命令を取り出す際に一時的に記憶する場所

- プラグラムカウンタ
- 命令レジスタ
- インデックスレジスタ
- ベースレジスタ
- アキュムレジスタ
- 汎用レジスタ

### 実行の命令手順
>
>1.命令の取り出し（フェッチ）
>
>2.命令の解読
>
>3.対象データ（オペランド）読み出し
>
>4.実行命令

## 機械語のアドレス指定方法

__実行アドレス__...計算によって求めたアドレス

__命令部__...何をするかの命令

__オペランド__...処理の対象となるデータの在処を示している

__アドレス指定__...実行アドレスを求める方式
>- 即値アドレス指定方式
>- 直接アドレス指定方式
>- 間接アドレス指定方式
>- インデックスアドレス指定方式
>- ベースアドレス指定方式
>- 相対アドレス指定方式

## CPUの性能指標

__クリック周波数__...クロックが1秒間に繰り返させる回数

__クリックサイクル時間__...一回のクリックにかかる時間

__CPL__...1命令あたりの必要なクリック数

__MIPS__...1秒間に実行できる命令の数

__命令ミックス__...よく使われる命令を1つのセットとした物

## CPUの高速化技術

__パイプライン処理__...複数の命令を並列して実行する方法

__分岐予測__...次の命令は何かを予測すること

__投機実行__...分岐先の命令を先にやること

__スーパーパイプライン__...細かい命令にすることで、効率を上げる

__スーパースカラ__...回路を複数作り、全く同時に複数の命令を実行できるようにした物

__CISC__...マイクロプログラムを記憶させて、高性能なマイ礼を実現する

__RISC__...ワイヤードロジックによってハードウェア的に実装した物

# chapter6 メモリ

## メモリの分類

### RAM(発揮性)
>DRAM
>
>SRAM
### ROM(不発揮性)
>マスクROM
>
>PROM
>
>>EPROM
>>
>>EEPROM
>>
>>フラッシュメモリ

## 主記憶装置と高速化手法

__キャッシュ__...記憶装置間の速度の間を埋める
>キャッシュメモリ
>
>ディスクキャッチ

### 主記憶装置への書き込む方式

1．ライトスルー方式

>キャシュメモリと同時に主記憶装置にも書き込みをする

2．ライトバック方式

>キャッシュメモリに書き込み、入らなくなったら、主記憶装置にうつす

### ヒット率と実行アクセス時間

___ヒット率__...目的とするデータがキャッシュメモリに入ってる確率

### メモリインタリーブ

__メモリインタリーブ__...主記憶装置野中を複数の区間に分け、複数の区間に同時にアクセスすることで、データを一気に読み込む

# chapter7 ハードディスクとその他の補助記憶装置

## ハードディスクの構造と記録方法

__プラッタ__...ハードディスクの中身

__セクタ__...ディスクの分けた区間の最小単位

__プラッタ__...セクタを複数並べて一週分の単位

__シリンダ__...トラックを複数まとめた単位

###　ハードディスクの記憶容量計算方法

> [!NOTE]
> セクタ　×　トラックのセクタ数　×　シリンダのトラック数　× シリンダ数　＝　記憶容量
>

__ファイルは、クラスタ（512b）という単位で操作する__


### データへのアクセスにかかる時間

> [!NOTE]
>回転速度　÷　回転回数　×　1/2　＝　平均サーチ時間
>
> 一トラック　÷　平均サーチ時間　＝　データ転送量
>
> 転送したい量　÷　データ転送量　＝　データ転送時間
>
> データ転送時間　＋　平均サーチ時間　＋　シーク時間　＝　アクセス時間

## フラグメーション　

__フラグメーション__...ファイルがあちこちに分かれて、断片化してしまう。

__デフラグメーション__...断片化したファイルを直す

## RAID

__RAID__...複数のハードディスクを使って、仮想的なハードディスクを構築、運用する
>
>RAIDO...1つのデータを2台以上のディスクに分散させて書き込む
>
>RAUD1...二台以上のディスクに常に同じデータを書き込む
>
>RAID5...3台以上のディスクを使ってデータとパリティを書き込む

## ハードディク以外の補助記憶装置

__リムーバブルメディア__...駆動装置から記憶媒体を簡単に取り外すことが出来る物

>- ###光ディスク
>> CDやDVDなど
>> 記録層に、レーザー光線を照射して、その反射をよみとる
>
>- ### 磁気テープ
>> テープを磁石で読み書きする
>
>- ### フラッシュメモリ
>> メモリカードやUSB
>
>- ### SSD
>> フラッシュメモリを記憶媒体として内蔵する装置

# その他のハードウェア

## 入力装置

- ### キーボード
- ### マウス
- ### トラックパット
- ### タッチパネル
- ### タブレット
- ### ジョイスティック

### 読み取り動作

- イメージスキャナ
- OCR
- OMR
- キャップチャカード
- デジタルカメラ
- バーコードリコーダ

### バーコードの規格

#### JANコード

__事業者コード　＋　商品アイテムコード　＋　チェックディジェット__

#### QRコード

__二次元コード__

#### RFID

__無線で読み取る__

## ディスプレイ

- CRTディスプレイ
- 液晶ディスプレイ
- 有機ELディスプレイ
- プラズマディスプレイ

## プリンタ

- ドットインパクトプリンタ
- インクジェットプリンタ
- レーザプリンタ

### プリンタの性能

__プリンタの解像度__
>dpiを使って表す
>1インチにどのくらいのドットで書かれるか

__プリンタの印字速度__
>cps...1秒間に何文字印刷できるか
>ppm...一分間に何ページ印字できるか

__3Dプリンタ__

1.熱溶解積層方式

2.光造形方式

## 入出力インタフェース

__入出力インターフェース__...ケーブルの規格

__プラグ・アンド・プレイ__...差し込めば使える仕組み

### 1.パラレル
> パラレルインタフェス(IDEE,SCSI)

### 2.シリアル
>シリアルインターフェス(USB,IEE1394)

### 3.無線インターフェス(IrDA,Bluetooth)
