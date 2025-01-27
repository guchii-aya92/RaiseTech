# 第4回課題

## 1.新規でVPCの作成、EC2とRDSの構築
VPCの作成はわからない単語が多かったですが録画講義を見ながらもできたので作成完了。
RDSもわりとすんなり構築できました。
EC2とRDSを接続しようともがいているときにEC2の作成時に設定を間違えていることに気づいたため作成し直しました。
その後コンソール画面から接続できましたが、課題内容と異なるため再トライ。
Cloud9を再構築してから行おうと思いましたが、方向転換しEC2でトライしました。
ました。MySQLインストール後、RDSに接続できました。
下記画像の赤線を参照ください。

![EC2からRDSへの接続確認](images/4-1.PNG)



## ファイルが空っぽだった理由
作成時に途中で編集ができなくなり、コマンドを打つこともできなかったので、
ページを閉じるという強硬手段を取りました。
その結果、途中で終了している状態？でスワップファイルになっており
中身が空になるということが起こりました。  
現在は復旧し、追記を書き加えています。


## 再提出後のやり直し
やり直しをして再プッシュしましたが、できていない模様…。
いったんブランチごと削除してやり直すことに。
今度はできていますように。


## エビデンスの再提出(2025/01/25)

### VPCの作成
VPC作成中の画面をスクショし忘れたため、コンソール画面のスクショです。

![VPCコンソール画面](images/4-2VPC.PNG)


### EC2の作成
EC2の画面をスクショしました。
作成時のものとコンソール画面です。

![EC2証左作成中](images/4-3EC2.png)

![EC2証左コンソール画面](images/4-4EC2.PNG)


### RDSの作成
RDSを作成中の画面をスクショしました。
またコンソール画面も乗せます。

![RDS証左作成中](images/4-5RDS.PNG)

![RDS証左コンソール画面](images/4-6RDS.PNG)


### セキュリティグループの作成
セキュリティグループの画面をスクショしました。

作成したセキュリティグループ・EC2
![セキュリティグループ証左EC2](images/4-7security-EC2.png)

作成したセキュリティグループ・database-1へアタッチ
![セキュリティグループ証左RDS](images/4-8security-database-1.PNG)

作成したセキュリティグループ・インスタンスへアタッチ
![セキュリティグループ証左instance](images/4-9security-instances.PNG)


### 追加の各種証左です(2025/01/27)
追加で提出依頼のあった証左です。


VPCのリソースマップ
![VPCのリソースマップ証左](images/4-10VPCresourcemap.PNG)


EC2詳細画面
![EC2詳細画面証左](images/4-11EC2detail.PNG)
![EC2詳細画面証左](images/4-12EC2detail.PNG)


RDSの接続とセキュリティの画面
![RDSの接続とセキュリティ](images/4-13RDSdetail.PNG)
![RDSの接続とセキュリティ](images/4-14RDSdetail.PNG)


サブネットグループ詳細画面
![subnet1apublic](images/4-15subnet1apiblic.PNG)
![subnet1aprivate](images/4-16subnet1aprivate.PNG)
![subnet1cpublic](images/4-17subnet1cpiblic.PNG)
![subnet1cprivate](images/4-17subnet1cprivate.PNG)


セキュリティグループのインバウンドルールとアウトバウンドルール
![inbound](images/4-18securitygruop-in.PNG)
![outbound](images/4-19securitygruop-out.PNG)

認識している構成を図にしてみました
![認識](images/4-0create.PNG)


