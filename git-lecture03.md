## 第３回課題報告書

#### 課題「サンプルアプリケーションのデプロイ」
![デプロイ](/test/picture/deploy.png)


#### APサーバーについて
プログラムで作られたアプリケーションを実行する為に必要なサーバー。

Ruby であれば Rails にも組み込まれている Puma が有名。

#### AP サーバーの名前とバージョンを確認してみましょう。
puma version 5.6.5 (ruby 3.1.2-p20)
![ＡＰサーバー](/test/picture/puma.png)

#### AP サーバーを終了させた場合、引き続きアクセスできますか?結果を確認して、また AP サーバーを起動してください。
サーバーを終了（停止＝contorol＋c）した状態ではアクセス出来ず、oopsと表示された。

再度起動（rails s）すると、アクセスできた。
![ＡＰサーバー](/test/picture/AP.png)

#### DBサーバーについて。サンプルアプリケーションで使った DB サーバー(DB エンジン)の名前と、今 Cloud9 で動作しているバージョンはいくつか確認してみましょう。
MySQL version: 8.0.34
![MySQL](/test/picture/MySQL.png)

#### DB サーバーを終了させた場合、引き続きアクセスできますか?
出来ず、oopsと表示される。下記コマンドを
- sudo service mysqld status　起動状態確認
- sudo service mysqld stop 停止
- sudo service mysqld start 起動
![DBサーバー停止](/test/picture/DB.png)

#### Railsの構成管理ツールの名前は何でしたか?
Bundler（メモ:今回のバージョンは bundler:2.3.14)
![Bundler](/test/picture/bundler.png)

#### 今回の課題から学んだことを報告してください。
- 講師のデモを見ながら、レクチャーの言葉と行程を照合させていった
- エラーには、どこがエラーが書かれてあり、まずは調べてみることが大切
- mysql.sockの場所を調べるには、mysql_configで調べられる
- データを書き換える際のルールに迷ったが、それがJsonかと気づいた

#### メモ
- ruby 3.0.6p216 (2023-03-30 revision 23a532679b) [x86_64-linux]
- rails 7.0.4