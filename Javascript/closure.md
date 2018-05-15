# Javascript Closure

내부함수는 외부함수의 지역변수에 접근 할 수 있는데 외부함수의 실행이 끝나서 외부함수가 소멸된 이후에도 내부함수가 외부함수의 변수에 접근 할 수 있다. 이러한 메커니즘을 클로저라고 한다.

```javascript
function factory_movie(title){
    return {
        get_title : function (){
            return title;
        },
        set_title : function(_title){
            title = _title
        }
    }
}
ghost = factory_movie('Ghost in the shell');
matrix = factory_movie('Matrix');
 
alert(ghost.get_title());
alert(matrix.get_title());
 
ghost.set_title('공각기동대');
 
alert(ghost.get_title());
alert(matrix.get_title());

```
factory_movie()의 title은 내부함수 set_title()로만 변경이 가능. 자바스크립트는 Private 개념이 없으므로 클로저 형태로 작성한다.

## reference
https://opentutorials.org/module/532/6544

https://developer.mozilla.org/ko/docs/JavaScript/Guide/Closures