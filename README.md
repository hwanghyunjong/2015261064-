# 2015261064 황현종

## 1. git 명령어

### 1.1 git에 대해서 사전에 알아야 될 부분

><pre> * git의 저장소는 3가지 단계로 나누어 집니다. 
> 커밋한 소스가 보관되는 저장소와 현재 프로젝트 파일들이 있는 작업트리, 
> 저장소와 작업트리사이의 버퍼영역으로 커밋될 대상이 저장되는 스테이징 영역입니다.
>
> * git은 빈 디렉토리는 추적하지 않습니다.
>
> * 형상관리를 하지 않을 파일은 .gitignore 파일에 추가합니다.
>
> * HEAD는 현재 브랜치의 가장 최신커밋을 의미한다.
>
> * 기본원격 저장소를 origin이라고 부릅니다. </pre>

### 1.1.1 commit 이란?
>git에서 commit는 내가 수정한 소스를 local 저장소에 반영

### 1.1.2 push 란?
>push는 내 local 저장소의 내용을 원격 저장소에 반영. 

### 1.1.1 pull 이란?
>pull는 원격 저장소의 내용을 local 저장소로 가져오는 것

### 1.2 환경설정
```sh
1. git config --global --list [현재 설정정보 조회할 수 있습니다.]
2. git config --global user.name "사용자명" [사용자명을 등록합니다 (필수)]
3. git config --global user.email "이메일주소" [이메일 주소를 등록합니다. (필수)]
4. git config --global color.ui “auto” [터미널에 표시되는 메시지에 칼라를 표시해줌]
```

### 1.3 기본적인 명령어
```sh
1. git --version [현재 git의 버전을 확인합니다.]
2. git init [현재 디렉토리에 git 저장소를 생성합니다.]
3. git add 파일명 [git add는 새로운 파일을 git에 등록시킵니다.]
4. git commit -m "커밋메시지" [스테이징 영역에 올라가 있는 파일들을 커밋(현재까지 작업한 내용 저장)]
5. git commit -C HEAD -a --amend [지정한 커밋의 로그메시지를 다시 사용하여 기존커밋을 수정합니다]
6. git checkout HEAD <파일> [<파일>] [작업 트리의 변경 사항 돌려놓기]
7. git reset HEAD <파일> [<파일>] [커밋되지 않고 스테이징된 변경 사항 재설정하기]
```

### 1.4 브랜치
```sh
1. git branch [지역 브랜치 목록 보기]
2. git branch -r "사용자명" [원격 브랜치 목록 보기]
3. git checkout <브랜치> [현재 브랜치에서 새로운 브랜치 생성하고 체크아웃하기]
4. git merge <브랜치> [커밋하지 않고 합치기]
5. git cherry-pick <커밋명> [커밋하지 않고 선택하여 합치기]
6. git branch -d <삭제할 브랜치> [브랜치 삭제하기] 삭제할 브랜치가 현재 브랜치에 합쳐졌을 경우에만
7. git branch -D <삭제할 브랜치> 삭제할 브랜치가 현재 브랜치에 합쳐지지 않았어도
```

### 1.5 원격 저장소
```sh
1. git clone <저장소> [저장소 복제하기]
2. git clone - -depth 200 <저장소> [새로운 원격 저장소 추가하기]
3. git fetch <원격 저장소> [원격 저장소에서 합치지 않고 지역 브랜치로 변경 사항 가져오기]
4. git pull <원격 저장소> [원격 저장소에서 변경 사항을 가져와 현재 브랜치에 합치기]
5. git push <원격 저장소> [새로운 로컬 브랜치를 원격 저장소에 푸싱하기]
```

### 1.6 TAG
```sh
1. git tag -a {tag name} -m {tag message} {commit hash} [태그 생성]
2. git tag -d {tag name}[태그 삭제]
3. git push origin --tags [태그 푸시]
```

## 2. Markdown 문법

