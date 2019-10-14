#### ・items一覧を取得する
HTTPメソッド： GET

リクエストURL： /api/v1/items

パラメータのデフォルト値：
```
"items": [
  {
    "id": 1,
    "name": "twitterの写真",
    "stock": 1,
    "content": "今日はセールス特売日です。よろしくお願いします。",
    "images": [
      {
        "image": "https://fashion-ec-web.s3-ap-northeast-1.amazonaws.com/uploads/item_image/image/18/lunch_time_for.jpg",
        "webp": "https://fashion-ec-web.s3-ap-northeast-1.amazonaws.com/uploads/items/src/18/lunch_time_for.webp"
      },
      {
        "image": "https://fashion-ec-web.s3-ap-northeast-1.amazonaws.com/uploads/item_image/image/19/lunch_time_for.jpg",
        "webp": "https://fashion-ec-web.s3-ap-northeast-1.amazonaws.com/uploads/items/src/19/lunch_time_for.webp"
      }
    ]
  },
  {
    "id": 2,
    "name": "twitterの写真",
    "stock": 1,
    "content": "今日はセールス特売日です。よろしくお願いします。",
    "images": [
      {
        "image": "https://fashion-ec-web.s3-ap-northeast-1.amazonaws.com/uploads/item_image/image/18/lunch_time_for.jpg",
        "webp": "https://fashion-ec-web.s3-ap-northeast-1.amazonaws.com/uploads/items/src/18/lunch_time_for.webp"
      },
      {
        "image": "https://fashion-ec-web.s3-ap-northeast-1.amazonaws.com/uploads/item_image/image/19/lunch_time_for.jpg",
        "webp": "https://fashion-ec-web.s3-ap-northeast-1.amazonaws.com/uploads/items/src/19/lunch_time_for.webp"
      }
    ]
  }
]
```
※ 入力パラメータによってレスポンス情報は変化する。

#### ・itemsを新しく作成する
HTTPメソッド： POST

リクエストURL： /api/v1/items

パラメータのデフォルト値：
```
"item": {
  "name": "名前",
  "content": "今日はセールス特売日です。よろしくお願いします。",
  "price": 1500,
  "stock": 1
  "item_image_attributes": [
    "image": "@/Users/hasegawataichiro/lunch_time_for.jpg;type=image/jpg"
  ]
}
```
※ 入力パラメータによってレスポンス情報は変化する。

#### ・1つのitemsを取得する
HTTPメソッド： GET

リクエストURL： /api/v1/items/:id
→ :idに対象のデータID

パラメータのデフォルト値：
```
"item": {
  "name": "名前",
  "content": "今日はセールス特売日です。よろしくお願いします。",
  "price": 1500,
  "stock": 1
  "item_image_attributes": [
    "image": "@/Users/hasegawataichiro/lunch_time_for.jpg;type=image/jpg"
  ]
}
```
※ 更新する入力パラメータのみを送る

#### ・itemsを更新する
HTTPメソッド： PUT

リクエストURL： /api/v1/items/:id
→ :idに対象のデータID

パラメータのデフォルト値：
```
"item": {
    "id": 1,
    "name": "twitterの写真",
    "stock": 1,
    "content": "今日はセールス特売日です。よろしくお願いします。",
    "images": [
      {
        "image": "https://fashion-ec-web.s3-ap-northeast-1.amazonaws.com/uploads/item_image/image/18/lunch_time_for.jpg",
        "webp": "https://fashion-ec-web.s3-ap-northeast-1.amazonaws.com/uploads/items/src/18/lunch_time_for.webp"
      },
      {
        "image": "https://fashion-ec-web.s3-ap-northeast-1.amazonaws.com/uploads/item_image/image/19/lunch_time_for.jpg",
        "webp": "https://fashion-ec-web.s3-ap-northeast-1.amazonaws.com/uploads/items/src/19/lunch_time_for.webp"
      }
}
```
※ 更新する入力パラメータのみを送る

#### ・itemsを削除する
HTTPメソッド： DELETE

リクエストURL： /api/v1/items/:id
→ :idに対象のデータID

※ 更新する入力パラメータのみを送る
