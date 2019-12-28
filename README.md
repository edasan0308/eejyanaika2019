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

データ形式は以下の様になっています。

```
//コンポーネントデータ
//RETURN
{
    "id": 1,
    "title": "ええじゃないか舞踊三昧 競舞部門・演舞部門",
    "place": "松葉公園・広小路通りほか",
    "charge": 0,
    "lat": "34.765812",
    "long": "137.385625",
    "tag": "見る",
    "info": "ええじゃないか舞踊三昧で今日を思いっきり楽しんで明日につなげていこう！",
    "start": "1970-01-01 00:00:00",
    "end": "1970-01-01 00:00:00",
    "url": "https://toyohashimatsuri.jp/images/butou/butou.jpg",
    "created_at": "2019-12-28 06:47:39",
    "updated_at": "2019-12-28 06:47:39"
}
    
//トイレデータ
//INPUT
{
	  "lat":34.323574,
	  "long":137.323443
}
//RETURN
{
    "id": 20,
    "title": "豊橋駅東口駅前",
    "lat": "34.764428",
    "long": "137.383179",
    "created_at": "2019-12-28 06:47:04",
    "updated_at": "2019-12-28 06:47:04"
}

//新たな登録時
INPUT
{
    "title": "ええじゃないか舞踊三昧 競舞部門・演舞部門",
    "place": "松葉公園・広小路通りほか",
    "charge": 0,
    "lat": "34.765812",
    "long": "137.385625",
    "tag": "見る",
    "info": "ええじゃないか舞踊三昧で今日を思いっきり楽しんで明日につなげていこう！",
    "start": "1970-01-01 00:00:00",
    "end": "1970-01-01 00:00:00",
}
RETURN
{
    "status":true
}
```
