# HTTPMethodTest
それぞれのHTTPメソッドでどんなやり取りが行われているか確認する。

# Setup
Node.jsをあらかじめインストール
~~~bash
node -v
v14.4.0

npm -v
6.14.5
~~~

json-serverのインストール
~~~bash
npm install -g json-server
~~~

json-server起動
~~~bash
json-server --watch db.json
~~~

# Methods
## GET
~~~bash
curl -X GET "http://localhost:3000/fruit" -v
~~~

## POST
~~~bash
curl -X POST -H "Content-Type: application/json" -d '{"id": 4, "name": "メロン"}' "http://localhost:3000/fruit" -v
~~~

## PUT
~~~bash
curl -X PUT -H "Content-Type: application/json" -d '{"id": 4, "name": "ウォーターメロン"}' "http://localhost:3000/fruit/4" -v
~~~

## DELETE
~~~bash
curl -X DELETE "http://localhost:3000/fruit/4" -v
~~~

## HEAD
~~~bash
curl -X HEAD "http://localhost:3000/fruit" -v
~~~

## OPTIONS
~~~bash
curl -X OPTIONS "http://localhost:3000/fruit" -v
~~~