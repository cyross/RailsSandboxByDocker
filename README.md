# RailsSandboxByDocker
めっちゃRailsのアプリ作りたいんやけどさっさとサンドボックス的な環境めっちゃほしーなーと思ったときに便利なDocker環境を作ってみようという企画です。単純にdocker-compose.yaml置いたら終わりと思うけど...

# インストール内容

* web
  * ruby2.6.4
  * rails6.0
  * Node.js8
  * Yarn
  * mysql8-communication
* db
  * mysql8

# 注意点

centosにインストールできるsqliteは3.7で、Railsで使用するsqliteのバージョンは3.8以上です。
しかし、sqliteはyumに依存しているため、おいそれと消せず、無理矢理3.8をインストールしてもgemでsqliteパッケージをインストールする際に混乱が考えられるため、Railsアプリを作る際はMySQLを使用するようにして下さい

```
rails new hoge --database=mysql
```

# 参考にしたリンク

* https://qiita.com/juhn/items/274e44ee80354a39d872
* https://qiita.com/tommy_aka_jps/items/b2ae85cbeab77e12a925
* Yarnのインストール https://qiita.com/seiyamaeda/items/18439866acf9ded9a2de
* Node.js8をcentos7にインストール https://qiita.com/you21979@github/items/4c9c382b9536effc590d
* centos7にMySQL8をインストール https://qiita.com/zaburo/items/7518a432d915c061983f
* yumがsqliteに依存している話 https://qiita.com/kai_kou/items/c18b68a7916251231f6d
