# 環境
環境毎の実装。

## 結論
コード上では環境による分岐をしてはいけない。  
機能フラグによる分岐をする。

## なぜか
`if (environement == 'production')` という分岐を書いてしまうと production 環境以外でデバッグができなくなる。  
当然 `switch (environment)` も同様。  

## どうするか
`if (feature)` という分岐にし、 config で環境毎に機能の ON/OFF を設定をする。
