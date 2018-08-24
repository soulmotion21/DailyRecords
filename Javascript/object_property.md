# Javascript object.property 

프로젝트 중 JSON 객체에 특수문자로 된 key의 value를 바인딩 할 수 없는 현상이 있어 관련하여 찾아보았다. 기본기는 이렇게 중요한 것이므로 기록해둔다.

- 속성 접근자(property accessor)는 점 또는 각괄호 표기법을 사용하여 객체 속성에 접근할 수 있다.



## 점 표기

```javascript
var obj = {
    "name": "John",
}

obj.name;

```


## 각괄호 표기

```javascript
var obj = {
    "<<": "ApplicationDefaults"
}

obj["<<"];

```



## reference
https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Operators/Property_Accessors