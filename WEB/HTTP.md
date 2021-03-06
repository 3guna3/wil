## HTTPとは
**Web上でクライアントとサーバーが通信するときのプロトコル**
- やり取りのインターフェースを統一することで分散システムが成立している

### HTTPはどういう決まり事なのか？
**決められた書式に則り、クライアントがHTTPリクエストを送り、サーバーがHTTPレスポンスを返す**

### HTTPリクエストとHTTPレスポンスの流れ
1. リクエストメッセージを作成(クライアント)
2. リクエストメッセージを送信(クライアント) 
3. リクエストメッセージを受信（サーバー）
4. リクエストメッセージを解析（サーバー）
5. アプリケーションへ処理を渡す（サーバー）
6. アプリケーションから結果をもらう（サーバー）
7. レスポンスメッセージを作成（サーバー）
8. レスポンスメッセージを送信（サーバー）
9. レスポンスメッセージを受信（クライアント）
10. レスポンスメッセージを解析(クライアント)

### HTTPメッセージの構造
**HTTPメッセージとはリクエストメッセージとレスポンスメッセージ両方**
```
GET / HTTP/1.1 #リクエストライン
Host: www.google.com:433 #ヘッダ
Accept: text/html
```
```
HTTP/1.1 200 # ステータスライン
cache-control: private, max-age=0 # ヘッダ
content-type: text/html; charset=UTF-8
date: Mon, 16 Nov 2020 21:41:35 GMT

<!doctype html><html lang="ja"> #　ボディ
<head><meta charset="UTF-8">...
```
