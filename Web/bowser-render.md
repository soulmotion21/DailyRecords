## 브라우저에 웹페이지가 로딩되는 과정 간략히 정리

1. 사용자가 브라우저 주소창에 url 입력 

2. DNS를 이용 사이트 IP주소에 접근 

3. 브라우저와 서버간 접속을 위한 TCP 소켓 연결 

4. 브라우저에서 HTTP 프로토콜로 Request 

5. 서버에서 요청받은 데이터 브라우저로 Response 

6. 브라우저의 html 코드가 파싱되어 DOM tree 생성됨 

7. css도 파싱되어 DOM tree와 함께 attachment 된 후 Render tree 생성 

8. layout에 따른 배치 및 렌더링 (painting) 

9. 사용자에게 보여짐 (display) 

10. 페이지의 DOM변경이 일어나면 painting시 reflow가 발생

   이 비용절감을 위해 현대 웹 앱에서는 Virtual DOM을 활용함 



## Reflow가 발생하는 케이스

1. insert, remove or update an element in the DOM 
2. modify content on the page, e.g. the text in an input box 
3. move a DOM element 
4. animate a DOM element 
5. take measurements of an element such as offsetHeight or getComputedStyle 
6. change a CSS style 
7. change the className of an element 
8. add or remove a stylesheet 
9. resize the window 
10. scroll




## reference

https://www.html5rocks.com/en/tutorials/internals/howbrowserswork