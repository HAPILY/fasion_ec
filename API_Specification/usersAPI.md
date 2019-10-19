#### ・ユーザーログインを行う
HTTPメソッド： POST

リクエストURL： /api/v1/login

パラメータのデフォルト値：
```
"data": {
  "email": "hasegawa@gmail.com",
  "password": "hasseiyeah"
}
```
※ 入力パラメータによってレスポンス情報は変化する。

#### ・ユーザーサインアップを行う
HTTPメソッド： POST

リクエストURL： /api/v1/users

パラメータのデフォルト値：
```
"data": {
"email": "hasegawa@gmail.com",
"password": "hasseiyeah",
"password_confirmation": "hasseiyeah",
"first_name": 長谷川,
"last_name": 太一朗,
"birthday": 1996-05-19
}
```

#### ・ユーザー情報一覧を取得する
HTTPメソッド： GET

リクエストURL： /api/v1/users

パラメータのデフォルト値：
```
"data": [
  {
    "id": 2,
    "first_name": "hasegawa",
    "last_name": "taichiro",
    "authority": "user",
    "birthday": "1996-05-19"
  },
  {
    "id": 1,
    "first_name": "hasegawa",
    "last_name": "taichiro",
    "email": "hasegawa@gmail.com",
    "authority_id": "user",
    "birthday": "1996-05-19"
  }
]
```
※ 入力パラメータによってレスポンス情報は変化する。

#### ・ユーザー情報一覧を取得する
HTTPメソッド： GET

リクエストURL： /api/v1/users/:id
→ :idに対象のデータID

パラメータのデフォルト値：
```
"data": {
  "id": 2,
  "first_name": "hasegawa",
  "last_name": "taichiro",
  "authority": "user",
  "birthday": "1996-05-19"
}
```
※ 入力パラメータによってレスポンス情報は変化する。

#### ・ユーザー情報を更新する
HTTPメソッド： PUT

リクエストURL： /api/v1/users/:id
→ :idに対象のデータID

パラメータのデフォルト値：
```
"data": {
  "email": "hasegawa@gmail.com",
  "password": "hasseiyeah",
  "password_confirmation": "hasseiyeah",
  "first_name": 長谷川,
  "last_name": 太一朗,
  "birthday": 1996-05-19
}
```
※ 入力パラメータによってレスポンス情報は変化する。

#### ・itemsを削除する
HTTPメソッド： DELETE

リクエストURL： /api/v1/items/:id
→ :idに対象のデータID

※ 更新する入力パラメータのみを送る
