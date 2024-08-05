## ①仮想環境の作成
```shell
python3 -m venv 仮想環境名
```
今回、venvと名前をつけた

## ②仮想環境の有効化
```shell
source 仮想環境名/bin/activate
```
これで仮想環境に入ることができます
### サーバーの起動
```
flask run
```
-pでポート番号、--reloadでファイル変更を監視したりできます。
また、flask 3.0.xからは--debugでデバッグモードにできます(2系は環境変数を設定するよ)

詳しくは、``flask run --help``

## ③仮想環境の無効化
```shell
deactivate
```

# Dockerでのイメージ作成&コンテナ実行

## ①イメージ作成
```
docker build --tag イメージ名:タグ名 .
```
``.``はDockerfileのある階層を指定。
タグ名を指定しなくても良い。

## ②コンテナ実行
```
docker run --publish 8000:5000 イメージ名
```
