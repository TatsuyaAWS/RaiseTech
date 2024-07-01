# 第5回課題

## サンプルアプリケーションの動作確認

- 組み込みサーバーによる動作確認
![組み込みサーバー](images05/test1.png)

- Unix Socketによる動作確認
![UnixSocket](images05/unixsocket.png)

- nginxの単体起動
![nginx](images05/nginx.png)

- nginxとpumaを組み合わせての動作確認
![nginxとpuma](images05/test2.png)

## EC2のセキュリティグループ

- インバウンドはSSHとELBからのHTTP接続のみ許可
![EC2セキュリティグループ](images05/ec2-secure.png)

## ALB接続

- ALB作成
![ALB](images05/alb.png)

- ALB接続確認
![ALB接続確認](images05/test3.png)

- ELBのセキュリティグループはHTTP接続のみ許可
![ELBセキュリティグループ](images05/elb-secure.png)

## s3に接続し、画像保存先に設定

- s3バケット作成
![s3](images05/s3.png)

- EC2にs3ロール権限付与
![s3ロール](images05/ec2-role.png)

- s3への保存確認
![s3へ保存](images05/save-test.png)

![保存確認](images05/s3-image.png)


## インフラ構成図
![構成図](images05/aws-architecture.png) 
