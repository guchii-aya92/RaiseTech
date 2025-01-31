# 第4回課題

## 1.新規でVPCの作成、EC2とRDSの構築
VPCの作成はわからない単語が多かったですが録画講義を見ながらもできたので作成完了。<br>
RDSも動画を見ながらだったのですんなり構築できました。<br>
EC2とRDSを接続しようともがいているときにEC2の作成時に設定を間違えていることに気づいたため作成し直しました。<br>
その後コンソール画面から接続できましたが、課題内容と異なるため再トライ。<br>
Cloud9を再構築してから行おうと思いましたが、方向転換しEC2でトライしました。<br>
MySQLインストール後、RDSに接続できました。下記画像の赤線を参照ください。

![EC2からRDSへの接続確認](images/4-1.PNG)


## ファイルが空っぽだった理由(2025/01/24)
作成時に途中で編集ができなくなり、コマンドを打つこともできなかったので、
ページを閉じるという強硬手段を取りました。<br>
その結果、途中で終了している状態？でスワップファイルになっており
中身が空になるということが起こりました。  
現在は復旧し、追記を書き加えています。


## 再提出後のやり直し(2025/01/24)
やり直しをして再プッシュしましたが、できていない模様…。<br>
いったんブランチごと削除してやり直すことに。
今度はできていますように。


## エビデンスの再提出(2025/01/25)
以下、構築物ごとに羅列します。

2. VPC
3. EC2
4. RDS

## 2.VPCの作成
VPC作成中の画面をスクショし忘れたため、コンソール画面のスクショです。
![VPCコンソール画面](images/4-2VPC.PNG)

### VPCのリソースマップ(2025/01/27)
![VPCのリソースマップ証左](images/4-10VPCresourcemap.PNG)

### サブネットグループ詳細画面
ap-northeast-1a-public
![subnet1apublic](images/4-15subnet1apiblic.PNG)
ap-northeast-1a-private
![subnet1aprivate](images/4-16subnet1aprivate.PNG)
ap-northeast-1c-public
![subnet1cpublic](images/4-17subnet1cpiblic.PNG)
ap-northeast-1c-private
![subnet1cprivate](images/4-17subnet1cprivate.PNG)




## 3.EC2の作成
EC2の画面をスクショしました。作成時のものとコンソール画面です。<br>
使用したVPCは上記で設定したものです。<br>
セキュリティグループは新規で作成しました。
![EC2証左作成中](images/4-3EC2.png)

作成したEC2と2詳細画面です。
![EC2証左コンソール画面](images/4-4EC2.PNG)
![EC2詳細画面証左](images/4-11EC2detail.PNG)
![EC2詳細画面証左](images/4-12EC2detail.PNG)


作成したセキュリティグループ・EC2
![セキュリティグループ証左EC2](images/4-7security-EC2.png)
![inbound](images/4-18securitygruop-in.PNG)
![outbound](images/4-19securitygruop-out.PNG)

セキュリティグループ・EC2インスタンスへアタッチ
![セキュリティグループtoinstance](images/4-9security-instances.PNG)
![セキュリティグループtoinstance](images/4-20securitygruoptoinstance.png)
  
## 4.RDSの作成
RDSを作成中の画面をスクショしました。
またコンソール画面も乗せます。

![RDS証左作成中](images/4-5RDS.PNG)

![RDS証左コンソール画面](images/4-13RDSdetail.PNG)
![RDS証左コンソール画面](images/4-14RDSdetail.PNG)


### セキュリティグループの作成
database-1へアタッチ
![セキュリティグループ証左RDS](images/4-8security-database-1.PNG)
![RDSインバウンドとアウトバンド](images/4-22securitygrouptodatabase1.PNG)
	
認識している構成を図にしてみました
![認識](images/4-0create.PNG)



