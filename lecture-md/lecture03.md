# 第3回課題

1. サンプルアプリケーションの起動
　　![サンプルアプリケーションの起動画面](images/sample-app.png)

2. APサーバーについて
    * APサーバーの名前：PUMA
    * バージョン：6.4.2
    * APサーバーを停止したとき：アプリは起動できない
    * ![APサーバー停止時](images/APserver-stop.png)
    * APサーバーの再起動成功
    * ![Pumaのバージョンと再起動](images/puma-version-restart.png)

3. DBサーバーについて
    * DBサーバーの名前：MySQL
    * バージョン：8.0.36
    * DBサーバーを停止したとき：アプリは起動できない
    * ![DBサーバー停止時](images/DBserver-stop.png)
    * DBサーバーの再起動成功
    * ![mysqlのバージョンと再起動](images/mysql-restart.png)
    * Railsの構成管理ツール：Bundler

## 第3回課題から学んだこと
* rubyやnodeなどのバージョンをしっかり確認しないと正しくサンプルが起動しないのでバージョンを確認するのを忘れない
* rubyのモジュールをgemと呼び、Bundlerという構成管理ツールで必要なライブラリと適切なバージョンをインストールできる
* アプリケーションサーバーとは、アプリを実行するためのサーバーであり、railsの組み込みサーバーがPumaである