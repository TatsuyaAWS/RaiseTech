# 第10回課題

セキュリティグループとそれ以外でスタックを分けております。

## 作成環境

### VPC
VPCにプライベートサブネットとパブリックサブネットを2つずつ作成。
![VPC](images10/vpc.png)

### EC2
- インスタンス
パブリックサブネットに設置し、S3アクセスロール付与
![EC2インスタンス](images10/ec2-1.png)
![EC2インスタンス](images10/ec2-2.png)

- セキュリティグループ
組み込みサーバーの3000ポートとHTTPをELBのセキュリティグループからの接続のみ許可,SSH,icmpのポートを自分のPCからの接続のみ許可
![EC2セキュリティグループ](images10/ec2security.png)

### RDS
- インスタンス
前回環境と同じためデフォルト
![RDSインスタンス](images10/rds.png)

- セキュリティグループ
3306ポートのEC2のセキュリティグループからの接続のみ許可
![RDSセキュリティグループ](images10/rdssecurity.png)

- 接続確認
![RDS接続確認](images10/mysql.png)

### IAMロール
S3へのアクセス許可をEC2に付与
![IAMロール](images10/iamrole.png)

### S3
- バケット
![S3バケット](images10/s3bucket.png)

- ポリシー
自分のPCからのアクセスを許可
![S3ポリシー](images10/bucketpolicy.png)

- 接続確認
S3バケット内の画像をダウンロード
![S3接続確認](images10/s3-download.png)

### ELB
- ロードバランサ―
アプリケーションロードバランサ―に設定し、2つのパブリックサブネットに振り分け
![ロードバランサ―](images10/roadbalancer.png)

- ターゲットグループ
組み込みサーバーで接続確認したため3000ポートにリッスン設定し、ヘルスチェック正常
![ターゲットグループ](images10/healthcheck.png)

- セキュリティグループ
3000ポートとHTTPのみ許可
![ELBセキュリティグループ](images10/elbsecurity.png)

