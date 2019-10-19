#### ・news一覧を取得する
HTTPメソッド： GET

リクエストURL： /api/v1/news

パラメータのデフォルト値：
```
"data": [
  {
    "id": 1,
    "title": "twitterの写真",
    "image": "https://fashion-ec-web.s3-ap-northeast-1.amazonaws.com/uploads/news/image/7/lunch_time_for.jpg",
    "webp": "https://fashion-ec-web.s3-ap-northeast-1.amazonaws.com/uploads/news/src/7/lunch_time_for.webp",
    "content": "今日はセールス特売日です。よろしくお願いします。",
    "category": "セールス"
  },
  {
    "id": 2,
    "title": "twitterの写真",
    "image": "https://fashion-ec-web.s3-ap-northeast-1.amazonaws.com/uploads/news/image/1/lunch_time_for.jpg",
    "webp": "https://fashion-ec-web.s3-ap-northeast-1.amazonaws.com/uploads/news/src/1/lunch_time_for.webp",
    "content": "今日はセールス特売日です。よろしくお願いします。",
    "category": "セールス"
  }
]
```
※ 入力パラメータによってレスポンス情報は変化する。

#### ・itemsを新しく作成する
HTTPメソッド： POST

リクエストURL： /api/v1/news

パラメータのデフォルト値：
```
"data": {
  "title": "twitterの写真",
  "image": "@/Users/hasegawataichiro/lunch_time_for.jpg;type=image/jpg",
  "content": "今日はセールス特売日です。よろしくお願いします。",
  "category": "セールス"
}
```
※ 入力パラメータによってレスポンス情報は変化する。

#### ・1つのitemsを取得する
HTTPメソッド： GET

リクエストURL： /api/v1/news/:id
→ :idに対象のデータID

パラメータのデフォルト値：
```
"data": {
  {
    "id": 1,
    "title": "twitterの写真",
    "image": "https://fashion-ec-web.s3-ap-northeast-1.amazonaws.com/uploads/news/image/7/lunch_time_for.jpg",
    "webp": "https://fashion-ec-web.s3-ap-northeast-1.amazonaws.com/uploads/news/src/7/lunch_time_for.webp",
    "content": "今日はセールス特売日です。よろしくお願いします。",
    "category": "セールス"
  }
}
```
※ 更新する入力パラメータのみを送る

#### ・itemsを更新する
HTTPメソッド： PUT

リクエストURL： /api/v1/news/:id
→ :idに対象のデータID

パラメータのデフォルト値：
```
"data": {
  "title": "twitterの写真",
  "image": "@/Users/hasegawataichiro/lunch_time_for.jpg;type=image/jpg",
  "content": "今日はセールス特売日です。よろしくお願いします。",
  "category": "セールス"
}
```
※ 更新する入力パラメータのみを送る

#### ・itemsを削除する
HTTPメソッド： DELETE

リクエストURL： /api/v1/news/:id
→ :idに対象のデータID

※ 更新する入力パラメータのみを送る
