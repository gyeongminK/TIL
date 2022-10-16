> branch 되돌리기
1. ```git reflog```로 커밋 내역 확인
2. 원하는 커밋 시점의 HEAD 번호 확인
3. ```git checkout -b <branch이름> <HEAD@{숫자}>``` 명령어로 해당 시점 브랜치 복구

또는 원하는 커밋 시점의 커밋 id를 확인해서
```git checkout <commit id>``` 명령어로 해당 시점으로 이동
