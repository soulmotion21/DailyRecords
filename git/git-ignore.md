## gitignore가 적용되지 않을 때

원격저장소에 add된 파일을 지우는 명령어
```shell
git rm -r --cached file-name
```

이 후 commit, push 해주면 된다.