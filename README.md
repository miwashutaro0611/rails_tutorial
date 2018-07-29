# メモ

## コンソール系
- start
```
$ rails c
```

- console内できること
```
User.first → Userの最初のデータ内容を取得する
User.all → Userの全件を取得する
first_user = User.first → User.firstの情報を変数first_userに格納する
```

- Railsのカラムの中身を確認する

```shell
User.columns
```
↑これだと他の情報も引っ張られるので、

```shell
User.columns.map(&:name)
```
か
```shell
User.column_names
```
で調べることができる

## url参照系

[scaffoldで作成したファイルを全削除](https://tamamemo.hatenablog.com/entry/20120113/1326435969)

[Railsコマンドでgenerateしたのを取り消したい場合](https://shinodogg.com/?p=3341)

[routesについて-](https://railsguides.jp/routing.html)

## ルール系

controllerは複数形
modelは単数形を使用する

## 実行させるまで

`bundle install`
`rails db:migrate`
`rails s`

# Railsチュートリアルについて

これは、次の教材で作られたサンプルアプリケーションです。   
[*Ruby on Rails チュートリアル*](https://railstutorial.jp/)
[Michael Hartl](http://www.michaelhartl.com/) 著

## ライセンス

[Ruby on Rails チュートリアル](https://railstutorial.jp/)内にある
ソースコードはMITライセンスとBeerwareライセンスのもとで公開されています。
詳細は [LICENSE.md](LICENSE.md) をご覧ください。

## 使い方

このアプリケーションを動かす場合は、まずはリポジトリを手元にクローンしてください。
その後、次のコマンドで必要になる RubyGems をインストールします。

```
$ bundle install --without production
```

その後、データベースへのマイグレーションを実行します。

```
$ rails db:migrate
```

最後に、テストを実行してうまく動いているかどうか確認してください。

```
$ rails test
```

テストが無事に通ったら、Railsサーバーを立ち上げる準備が整っているはずです。

```
$ rails server
```

詳しくは、[*Ruby on Rails チュートリアル*](https://railstutorial.jp/)
を参考にしてください。
