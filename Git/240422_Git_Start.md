## Git이란?
- 스냅샷 모델
- 델타와 스냅샷의 비교

|델타|스냅샷|
|:---:|:---:|
|변경점만을 기록하는 방식|변경점도 기록하고, 수정되지 않더라도 기록을 남김|
|이전 버전과 비교하고 복원 시점을 찾을때 굉장히 느림|수정되지 않았을때는 이전 파일의 링크만 참조함 (복원이 빠름)|

## .git 디렉토리
- . 의 의미는 숨겨져있는 폴더라는 의미
- 디렉토리 안에 git이 관리하는 변경 이력이 다 담겨있음
- 저장소라고 부름 (= git 저장소)
- `git init` : 일반 폴더를 깃 저장소로 만들어줌 → .git이라는 폴더가 생성됨
- Git이 관리하는 저장소의 기본 브랜치가 master일 경우 main으로 변경할 수 있다

```
# git init 명령으로 생성된 저장소의 기본 브랜치가 master일 때 main으로 브랜치명을 변경
git branch -m main

# git init 명령으로 Git 저장소를 초기화 시킬 때 브랜치가 main이 되도록 설정
git init -b main

# 로컬 환경에서 git init 명령을 통해 Git 저장소를 초기화하면 기본 브랜치가 main이 되도록 설정 
git config --global init.defaultBranch main
```

- `git restore` : 워킹 디렉토리에서 수정된 내용 삭제하는 명령어
- 한번도 커밋한적없으면 `rm —cached`
- 한번이라도 커밋된것이면 `restore —staged`
- git 명령어 단축키 설정하려면 `git alias` 설정