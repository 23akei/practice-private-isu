# private-isu-practice
[private-isu](https://github.com/catatsuy/private-isu)を利用した練習用リポジトリ。

## 環境
* Machine: Macbook Air M1 2020, 16GB RAM
* Running on: Orbstack


## initial score
(失敗)

言語：Ruby
```
{"pass":false,"score":0,"success":9,"fail":8,"messages":["response code should be 403, got 200 (GET /login)","ステータスコードが正しくありません: expected 422, got 200 (GET /login)","ユーザー名が表示されていません (GET /)","リダsts/9391$', got '/login' (GET /login)","リダイレクト先URLが正しくありません: expected '^/posts/\\d+$', got '/login' (GET /login)","ログインエラーメッセージが表示されていません (GET /login)"]}
```


### docker compose修正後
See: https://github.com/catatsuy/private-isu/pull/425

言語：PHP(以降同じ)
```
{"pass":true,"score":0,"success":121,"fail":64,"messages":["リクエストがタイムアウトしました (GET /)","リクエストがタイムアウトしました (GET /image/10000.png)","リクエストがタイムアウトしました (GET /image/10012.jpg)","リクエスた (GET /image/4764.jpg)","リクエストがタイムアウトしました (GET /image/6239.jpg)","リクエストがタイムアウトしました (GET /image/7962.jpg)","リクエストがタイムアウトしました (GET /image/8510.gif)","リクエストがタイムアウトしまし","リクエストがタイムアウトしました (GET /image/9057.jpg)","リクエストがタイムアウトしました (GET /image/9216.gif)","リクエストがタイムアウトしました (GET /image/9359.jpg)","リクエストがタイムアウトしました (GET /image/9996.jpgストがタイムアウトしました (GET /image/9997.jpg)","リクエストがタイムアウトしました (GET /image/9998.jpg)","リクエストがタイムアウトしました (GET /image/9999.jpg)","リクエストがタイムアウトしました (POST /login)","リクエストがタイムアウトしました (POST /register)"]}
```

## fix and score
### DBアクセスの改善：postsデータの作成
See: https://github.com/23akei/practice-private-isu/pull/2

変更後のベンチマーク結果
```
{"pass":true,"score":1614,"success":1502,"fail":1,"messages":["ステータスコードが正しくありません: expected 200, got 404 (GET /posts/10022)"]}
```

## まとめ
まず、変更箇所の候補として
* Webサーバの改善
* DBスキーマの改善
* アプリケーションロジックの改善
* キャッシュの改善

が考えられた。その中で今回は自分でも簡単にできそうなアプリケーションロジックの改善を行うことにした。

最初にとりあえずアプリケーションを立ち上げて、ブラウザからアクセスした。そこでトップページの読み込みが遅いことを発見し、
https://github.com/23akei/practice-private-isu/pull/2 の変更に至った。

今回はブラウザの開発者ツール以外で時間計測やその他パフォーマンス計測を行わなかった。
さらなる改善のためにはこれらを利用していく必要があると考える。
