[DXを大幅に低下させるDocker for Macを捨ててMac最速のDocker環境を手に入れる](https://qiita.com/yuki_ycino/items/cb21cf91a39ddd61f484) 参照  

VM上にdockerコンテナを起動し、ローカルにhasura環境を作成する

## 下準備
・ホストドメインを設定
  `$ sudo vim ~/private/etc/hosts` → 使用するIPとローカルドメインを関連づける
・vagrant-disksize, vagrant-hostsupdater, vagrant-mutagenのインストール(なければ)
  `$ vagrant plugin install vagrant-disksize vagrant-hostsupdater vagrant-mutagen`
・Mutagenのインストール(なければ)
  `$ brew install mutagen-io/mutagen/mutagen ` 

## 操作
・VM起動
  `$ vagrant up`
・VMにsshログイン
  `$ vagrant up`
・(VM内で)appに移動
  `# cd app`
・コンテナ立ち上げ
  `# docker-compose up -d`
・指定されたIPにhasuraコンソールが立ち上がっている
  `# docker ps` → `http://localhost:8080/console`
