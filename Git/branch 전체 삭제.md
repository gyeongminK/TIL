git branch 일부만 제외하고 전체 삭제하는 방법
> ```git branch | grep -v "(남길 브랜치명1)" | grep -v "(남길 브랜치명2)" | xargs git branch -D``` <br>
