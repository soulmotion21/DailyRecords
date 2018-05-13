# Javascript Prototype

- prototype이란 번역하면 '원형'과 같은 의미이다.
- 자바스크립트에선 객체의 원형을 의미하는 property로 모든 객체는 이 property를 가질 수 있다.
- prototype에 저장된 속성들은 생성자를 통해 객체가 만들어질 때 그 객체에 연결될 수 있다.
- 이 때 생성하기 위해 사용된 객체원형을 prototype이라 한다.

## 자바스크립트의 Prototype
```javascript
function Ultra(){}
Ultra.prototype.ultraProp = true;
 
function Super(){}
Super.prototype = new Ultra();
 
function Sub(){}
Sub.prototype = new Super();
 
var o = new Sub();
console.log(o.ultraProp);
```
- 결과는 true다. new 생성자 함수를 통해 Ultra부터 아래로 계속 상속되고 있다. 이를 prototype chaining이라고 한다.
- 주의할 점은 new 생성자 함수를 사용하지 않으면 상속을 받을 수 없고 심지어 상속받은 객체의 prototype도 바뀌게 된다
- ex) Super.prototype = Ultra.prototype (X)

## reference
https://opentutorials.org/course/743/6573

https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/Inheritance_and_the_prototype_chain

http://insanehong.kr/post/javascript-prototype/