# tag replace

가끔 데이터 바인딩 중에 html 태그가 있을 경우 태그를 제거하는 방법이 필요한데 이 때 태그를 제거하는 정규식.

## object

```javascript
var obj = {"contents": "<p>abcd</p>"}

var str = obj.contents;
str.replace(/(<([^>]+)>)/ig, "")
```

