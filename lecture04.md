# 第4回課題

### VPCの作成
* 今回は動作確認のため最低限VPCとパブリック・プライベートサブネットとIGWを作成しました。
![VPC作成エビデンス](img-lecture04/resourcemap.png)

### EC2の作成
* OSはAmazonLinux2にしました。
![EC2概要](img-lecture04/ec2-info.png)
* セキュリティグループは動作確認に必要な自分のIPからのSSHとping疎通のためのICMPを許可するよう作成しました。
![EC2セキュリティグループ](img-lecture04/ec2-security.png)

### RDSの作成
* MySQLを選択、無料利用枠のテンプレートで作成しました。
![RDS概要](img-lecture04/rds-info.png)
* VPCは最初に作成したものを選択し、VPCセキュリティグループはEC2からの接続のみを許可するよう設定しました。
![RDSインバウンドセキュリティグループ](img-lecture04/rds-security-in.png)
![RDSアウトバウンドセキュリティグループ](img-lecture04/rds-security-out.png)

### EC2からRDSの接続確認
![EC2からRDSの接続エビデンス](img-lecture04/ec2-rds-connect.png)