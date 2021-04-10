# Finding index by key, value  

언젠가 작업 중에 객체의 특정 key, value값으로 index를 찾아야 하는 경우가 생겼다. 그 때 찾아보고 써먹었던 방법을 기록함. map, indexOf도 이용할 수 있었으나 그냥 해봤다.

## object

```json
var arr = [{"type": "block"},{"type": "org"}]
```



## function

- 배열을 조회해서 해당 키의 밸류를 찾아 인덱스를 반환

```javascript
var nIdx = fnTofindIndexByKeyValue(arr, "type", "org"); // 1

function fnTofindIndexByKeyValue(arraytosearch, key, valuetosearch) {
  for (var i = 0; i < arraytosearch.length; i++) {
    if (arraytosearch[i][key] === valuetosearch) {
      return i;
    }
  }
  return null;
}
```





