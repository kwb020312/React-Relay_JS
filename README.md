# React & GraphQL & Relay

<img src="gitImages\Relay_Logo.jpg">

※ 해당 저장소는 Relay 의 <a href="https://relay.dev/">공식문서</a>를 보고 참고하여 만들어졌음을 밝힙니다.

- 본 Repository에선 <a href="https://graphql.org/">GraphQL</a>을 기본적으로 다룰 줄 안다는 가정하에 진행되니 모르는 분들은 학습하시길 바랍니다.

RESTFUL API 를 사용하는 과정에서 GraphQL뿐만이 아닌 Relay 또한 인기가 급등하고 있는데 해당 Repository에선 어떠한 이점으로 인기가 오를 수 있었는지 자세하게 알아보겠다.

## 설치과정

```javascript
// relay & graphql
yarn add --dev babel-plugin-relay graphql
```

이제 불러올 때는

```javascript
const graphql = require("babel-plugin-relay/macro");
```

로 불러올 수 있다.

이 후 컴파일러를 설치하고

```javascript
yarn add --dev relay--compiler
```

나의 경우 GraphQL을 미리 설정해두었으므로 자신의 GraphQL을 가져다 쓰면 됨

<img src="gitImages\Graphql_Source.jpg">

```javascript
"scripts" : {
    "relay": "relay-compiler --src ./src --schema ./schema.graphql --extensions js jsx"
}
```

```javascript
// watch옵션은 해당 GraphQL소스가 변경될 때 마다 반영함
yarn run relay --watch
```
