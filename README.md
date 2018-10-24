# 2015261064 황현종

## 1. git 명령어

### git에 대해서 사전에 알아야 될 부분

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

### 환경설정
><pre> git config --global --list 
>현재 설정정보 조회할 수 있습니다. --global옵션은 전역설정에 대한 옵션이며 현재 프로젝트에만 적용할때는 주지 않습니다.
>git config --global user.name "사용자명" 
>사용자명을 등록합니다 (필수)
>git config --global user.email "이메일주소" 
>이메일 주소를 등록합니다. (필수)
>git config --global color.ui “auto”
>터미널에 표시되는 메시지에 칼라를 표시해줌</pre>

### 기본적인 명령어
<pre>
> **git --version**
> 현재 git의 버전을 확인합니다.

> git init
> 현재 디렉토리에 git 저장소를 생성합니다.

> git add 파일명
> git add는 2가지를 하는데 untracked files의 파일들을 git가 추적하도록 하거나 파일은 수정했지만 아직 스테이징 영역에 올라가지 않은(Changed but not > updated) 파일들을 스테이징 영역에 올립니다. -i 옵션을 주면 대화형모드가 시작되며 파일의 일부분만 선택해서 스테이징하는 것이 가능합니다. -p 옵션을 > > 사용하면 -i 대화형모드없이 바로 패치모드를 사용할 수 있습니다.

</pre>



