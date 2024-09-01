# プログラミング言語

## 実行方法

### インタプリタ方式

命令を一つずつ実行する

### コンパライア方式

命令全体を実行する

# コンパイラ方式

### コンパイラ

ソースコードを機械語に翻訳する

### リンカ

モジュール等をつなぐ仕事をする（リンク）

### ローダ

ロードモジュールを主記憶に読み込ませる仕事をする

# 変数

### 宣伝方法

型名：変数名

変数名　←　式

## 構造化プログラミング

### 制御構造
>
>順次構造
>
>選択構造
>>
>>if ~ endifで表す
>
>繰り返し構造
>>
>>white ~ endwhiteで前判定の繰り返し構造を表す
>>
>>do ~ whileで後判定の繰り返し構造を表す
>>
>>for ~ endforで繰り返し構造を表す
>

# アルゴリズム

### アルゴリズム

プログラムの処理手順

### フローチャート

アルゴリズムをわかりやすく表す図

# データの持ち方

### データ構造

データを配置する方法

## 配列

### 添え字

配列のような連続したデータにある番号

### 一次元配列

普通の配列

### 多次元、二次元配列

二次元配列だと、縦と横で表す

## リスト

### リスト

データとデータをつないで管理する

### ポインタ

リストにある、次のデータがどこにあるかを書いた数字

### リストの種類
>
>単方向リスト
>
>双方向リスト
>
>循環リスト

## キュー

FIFO方式のデータ構造

## スタック

LIFO方式のデータ構造

# ツリー構造

## 2分木

### 2分木

節からののびる枝が二本以下であるものを2分木とよぶ

### 完全2分木

葉以外の節がすべて2つの子を持ち、根から葉までの深さが等しい2分木のこと

### 2分探索木

左の子＜親＜右の子になる2分木

# データを探索するアルゴリズム

### 線型探索法

先頭から順に探していく

### 2分探索法

降順、昇順に並んでいるものを調べるときに使う
真ん中の文字と探している文字を比較して探していく

### ハッシュ法

ハッシュ関数を用いて、場所を特定する

# データを整列させるアルゴリズム

### バブルソート

隣り合わせたデータを比較して、交換していく

### 選択ソート

最小または最大のデータを取りだすことを繰り返して整列させる

### 挿入ソート

整列済みと未整列を分けて、データを一つずつ整列済みの適切な位置に挿入する方法

### シェルソート

一定間隔で取り出して、それぞれの中で、整列一つに戻す。を繰り返す

### クイックソート

基準値を決めて、大小でグループを分けて....を繰り返す

### ヒープソート

順列木を作成して根を取り出して、整列させていく

# オーダ記法

### オーダ

処理するデータ量によってアルゴリズムに要する実行時間を表す概念

### 各種のオーダ
>
>線型探索法　      ０(n)
>
>2分探索法      ０(log2n)
>
>ハッシュ法　        ０(1)
>
>バブルソート　    ０(n²)
>
>選択ソート　    ０(n²)
>
>挿入ソート　    ０(n²)
>
>シェルソート    　０(n1.2)
>
>クイックソート    　０(nlog2n)
>
>ヒープソート    　０(nlog2n)

# オブジェクト指向プログラミング

### オブジェクト

データとメソッドを一つにまとめた概念

### データ

属性

### メソッド

手続き

### カプセル化

データとメソッドをひとまとめの構造にする。
情報隠蔽ができる

## クラスとインスタンス

### クラス

オブジェクトが持つ性質を定義したもの

### 継承（インヘリタンス）

サブクラスがスーパークラスの特性を受け継ぐこと

## 関係

### 汎化と特化（is a関係）

上位が汎化、下位が特化している関係

### 集約と分解（part of 関係）

上位が集約、下位が分解している関係

# UML

### 構造図

システム構造を表す

### ふるまい図

システムのふるまいを表す

### クラス図

クラスの定義や関連付けを示す図

### ユースケース図

利用者視点でシステムが要求に対してどのようにふるまうかを示す図

### アクティビティ図

業務や処理のフローを表す図

### シーケンス図

オブジェクト間のやり取りを時系列順にそって表す図