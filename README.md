# private-isu-practice
[private-isu](https://github.com/catatsuy/private-isu)を利用した練習用リポジトリ。

## 環境
* Machine: Macbook Air M1 2020, 16GB RAM
* Running on: Orbstack


## initial score
* Language: Ruby
  (失敗)
```
{"pass":false,"score":0,"success":9,"fail":8,"messages":["response code should be 403, got 200 (GET /login)","ステータスコードが正しくありません: expected 422, got 200 (GET /login)","ユーザー名が表示されていません (GET /)","リダsts/9391$', got '/login' (GET /login)","リダイレクト先URLが正しくありません: expected '^/posts/\\d+$', got '/login' (GET /login)","ログインエラーメッセージが表示されていません (GET /login)"]}
```

* Language: PHP
修正後(成功)
```
{"pass":true,"score":0,"success":121,"fail":64,"messages":["リクエストがタイムアウトしました (GET /)","リクエストがタイムアウトしました (GET /image/10000.png)","リクエストがタイムアウトしました (GET /image/10012.jpg)","リクエスた (GET /image/4764.jpg)","リクエストがタイムアウトしました (GET /image/6239.jpg)","リクエストがタイムアウトしました (GET /image/7962.jpg)","リクエストがタイムアウトしました (GET /image/8510.gif)","リクエストがタイムアウトしまし","リクエストがタイムアウトしました (GET /image/9057.jpg)","リクエストがタイムアウトしました (GET /image/9216.gif)","リクエストがタイムアウトしました (GET /image/9359.jpg)","リクエストがタイムアウトしました (GET /image/9996.jpgストがタイムアウトしました (GET /image/9997.jpg)","リクエストがタイムアウトしました (GET /image/9998.jpg)","リクエストがタイムアウトしました (GET /image/9999.jpg)","リクエストがタイムアウトしました (POST /login)","リクエストがタイムアウトしました (POST /register)"]}
```
