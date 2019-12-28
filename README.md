# eejyanaika2019
ええじゃないか学生ハッカソンin豊橋で作成したPersonerです。
`/front/`でnpmが使える状態で

```
npm run serve --https
```

とすることでwebサーバを立ち上げられます。
API側は https://floating-anchorage-00104.herokuapp.com/ に既にデプロイされているので、そちらをご利用ください。以下利用方法です。

```

//全件取得してくる場合
Method:GET
https://floating-anchorage-00104.herokuapp.com/components

//id指定で一件取得してくる場合
Method:GET
https://floating-anchorage-00104.herokuapp.com/components/{id}

//ユーザーの位置情報から一番近いトイレ情報を取得してくる場合
Method:POST
https://floating-anchorage-00104.herokuapp.com/components/toilet/get
json{"lat":22.44, "long":33.45}

//ユーザーが新たなコンポーネントを登録する場合
Method:POST
https://floating-anchorage-00104.herokuapp.com/components/create
json{"title":"aaa",lat":22.44, "long":33.45  .......}

```
