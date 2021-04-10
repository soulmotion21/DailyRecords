# Optional chaining

- ?. 연산자는 뎁스가 깊은 객체의 참조들이 유효한지 간편하게 확인이 가능하게 함.
- 참조가 nullish (null, undefined) 일 경우 undefined를 리턴
- es2020 스펙

## example

```javascript
// props.data를 먼저 확인
const user = props.data && props.data.defaultMeta.user

// ?. 연산자로 간편하게 가능
const user = props.data?.defaultMeta.user

if (!user) {
  ....
}
...

```


## reference
https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Operators/Optional_chaining