# SSH

## 問題

シス研のローカルネットワークにipv4アドレス(1.1.1.1)を割り当てたサーバが有ります.
ipアドレスでのアクセスでは操作ミスの原因になりかねないので名前解決をすることにしました.
hoge.comでリクエストした時に1.1.1.1を返すdnsサーバを構築してください. 


## 補足

- dnsサーバにはdnsmasqを利用すること
- ドメイン名はhoge.comにすること
- 名前解決できているかはdig or nslookupコマンドで確認することができます.
- docker for macで構築しているためdnsサーバのipアドレスは127.0.0.1になります.
- answer.pngのようになっていれば正解です(digコマンドを使用しています)

## コマンド

- `make up`

  - コンテナを起動します．はじめにこれを実行してください．

- `make sh`
  - コンテナ上で bash を起動し，操作できるようにします．

## 採点項目

- dnsmasqをインストールしているか？
- dnsmasqが起動しているか？
- dnsのレコードが正しく設定されているか？
- hoge.comに対してdigコマンドで実行した場合,1.1.1.1が返ってくるか？