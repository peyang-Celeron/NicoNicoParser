# NicoNicoParser

## 概要

ニコニコ大百科と掲示板データを分かち書き可能なレベルまでパースします。

## 動作環境
+ Python 3.7+

### MecabSplit
大きいファイルを分割/並列化して処理し、OSをハングさせることなく巨大ファイルのMecabを実行します。

#### 使用法

+ 1.書き換え
```
$ python mecab.py
```
+ 2.年を入力  
大百科とかのパースで、年ごとにファイルが違うことがあるため
+ 3.待つ  
CPUの性能で大幅に変わります。(メモリは1GBもいりません)
+ 4.2に戻る

### EntityReferencesFixer

HTMLの特殊文字を削除します。
+ MecabSplitを実行した後に、同じフォルダで実行すると、期待される動作を致します。

+ 1.書き換え
```
$ python entityreferencesfixer.py
```
+ 2.年を入力  
大百科とかのパースで、年ごとにファイルが違うことがあるため
+ 3.待つ  
CPUの性能で大幅に変わります。(メモリは1GBもいりません)
+ 4.2に戻る

### NicoNicoIME2Mecab

ニコニコ大百科IME辞書\(通称ニコニコIME\)を、Mecabが読める状態までパースします。  
+ Microsoft IME 用のインプットファイルが動作します。

#### 使用法

+ 1.書き換え
```
5: fname = "niconicoime_msime.txt" => 自分が持つファイルに変更
```
+ 2.実行
```
$ python ms2ime.py
```
### NicoNicoExtractor

#### 使用法

+ 1.実行  
```
$ python nikonikoparser.py
```
+ 2.年を入力  
大百科とかのパースで、年ごとにファイルが違うことがあるため  
+ 3.待つ  
CPUの性能で大幅に変わります。(メモリは1GBもいりません)  

### 作成されるディレクトリとか

+ complete  
パースされたデータが入ります。すべて完了すると、../<year>.archive として保存されます。  
