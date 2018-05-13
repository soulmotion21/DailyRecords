## OS X Sierra 부터 Adobe CS 5.5 설치 안될 때

정식 라이센스를 가지고 있는 Adobe CS 5.5가 시에라 부터 지원을 하지 않는다. 가능한 정식 버전을 계속 쓰고 싶어 검색해 보니 해결책이 있었다.

1. Right click on the app(install) and go to 'Show Package Contents'  

   (볼륨디스크에 install.app 파일 우클릭 -> 패키지 내용 보기)

2. Navigate to 'Contents/MacOS' and open that folder in Terminal 

   (터미널 열고 Contents/MacOS 경로로 이동. 커맨드 + 드래그로 터미널 창에)

3. 터미널에 install 명령어 혹은 install 실행

```shell
sungkyukimui-MacBook-Pro:~ sungkyukim$ cd /Volumes/CS5_5\ Web\ Prm/Adobe\ CS5_5\ Web\ Premium/Install.app/Contents/MacOS 

sungkyukimui-MacBook-Pro:MacOS sungkyukim$ sudo ./Install
```



## reference

https://helpx.adobe.com/creative-cloud/kb/install-creative-suite-mac-os-sierra.html#CreativeSuite555and4