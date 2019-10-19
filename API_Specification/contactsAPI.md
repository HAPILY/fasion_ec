#### ・お問い合わせ一覧を取得する
HTTPメソッド： GET

リクエストURL： /api/v1/contacts

パラメータのデフォルト値：
```
"data": [
  {
    "id": 1,
    "name": "長谷川太一郎",
    "email": "hasegawa@gmail.com",
    "content": "今日はセールス特売日です。よろしくお願いします。"
  },
  {
    "id": 2,
    "name": "長谷川太一郎",
    "email": "taichiro@gmail.com",
    "content": "今日はセールス特売日です。よろしくお願いします。"
  }
]
```
※ 入力パラメータによってレスポンス情報は変化する。

#### ・1つのお問い合わせ一覧を取得する
HTTPメソッド： GET

リクエストURL： /api/v1/contacts/:id
→ :idに対象のデータID

パラメータのデフォルト値：
```
"data": {
  "id": 1,
  "name": "長谷川太一郎",
  "email": "hasegawa@gmail.com",
  "content": "今日はセールス特売日です。よろしくお願いします。"
}
```
※ 入力パラメータによってレスポンス情報は変化する。

#### ・お問い合わせする
HTTPメソッド： POST

リクエストURL： /api/v1/contacts

パラメータのデフォルト値：
```
"data": {
  "name": "長谷川太一郎",
  "email": "hasegawa@gmail.com",
  "content": "今日はセールス特売日です。よろしくお願いします。"
}
```
※ 入力パラメータによってレスポンス情報は変化する。
