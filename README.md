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

### 2.1 마크다운이란?
>[**Markdown**]은 텍스트 기반의 마크업언어로 2004년 존그루버에 의해 만들어졌으며 쉽게 쓰고 읽을 수 있으며 HTML로 변환이 가능하다. 특수기호와 문자>를 이용한 매우 간단한 구조의 문법을 사용하여 웹에서도 보다 빠르게 컨텐츠를 작성하고 보다 직관적으로 인식할 수 있다.
>마크다운이 최근 각광받기 시작한 이유는 깃헙([https://github.com](https://github.com)) 덕분이다. 깃헙의 저장소Repository에 관한 정보를 기록하는 >README.md는 깃헙을 사용하는 사람이라면 누구나 가장 먼저 접하게 되는 마크다운 문서였다. 마크다운을 통해서 설치방법, 소스코드 설명, 이슈 등을 간단>>하게 기록하고 가독성을 높일 수 있다는 강점이 부각되면서 점점 여러 곳으로 퍼져가게 된다.

## 2.2. 마크다운의 장-단점
### 2.2.1. 장점
	1. 간결하다.
	2. 별도의 도구없이 작성가능하다.
	3. 다양한 형태로 변환이 가능하다.
	3. 텍스트(Text)로 저장되기 때문에 용량이 적어 보관이 용이하다.
	4. 텍스트파일이기 때문에 버전관리시스템을 이용하여 변경이력을 관리할 수 있다.
	5. 지원하는 프로그램과 플랫폼이 다양하다.
### 2.2.2. 단점
	1. 표준이 없다.
	2. 표준이 없기 때문에 도구에 따라서 변환방식이나 생성물이 다르다.
	3. 모든 HTML 마크업을 대신하지 못한다.
****
# 2. 마크다운 사용법(문법)
## 2.1. 헤더Headers
* 큰제목: 문서 제목
    ```
    This is an H1
    =============
    ```
    This is an H1
    =============

* 작은제목: 문서 부제목
    ```
    This is an H2
    -------------
    ```
    This is an H2
    -------------

* 글머리: 1~6까지만 지원
```
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
```
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
####### This is a 7.

## 2.2. BlockQuote
이메일에서 사용하는 ```>``` 블럭인용문자를 이용한다.
```
> This is a blockqute.
```
> This is a first blockqute.
>	> This is a second blockqute.
>	>	> This is a third blockqute.

이 안에서는 다른 마크다운 요소를 포함할 수 있다.
> ### This is a H3
> * List
>	```
>	code
>	```

## 2.3. 목록
### ● 순서있는 목록(번호)
순서있는 목록은 숫자와 점을 사용한다.
```
1. 첫번째
2. 두번째
3. 세번째
```
1. 첫번째
2. 두번째
3. 세번째

**현재까지는 어떤 번호를 입력해도 순서는 내림차순으로 정의된다.**
```
1. 첫번째
3. 세번째
2. 두번째
```
1. 첫번째
3. 세번째
2. 두번째

딱히 개선될 것 같지는 않다. 존 그루버가 신경안쓰고 있다고...

### ● 순서없는 목록(글머리 기호)
```
* 빨강
  * 녹색
    * 파랑

+ 빨강
  + 녹색
    + 파랑

- 빨강
  - 녹색
    - 파랑
```
* 빨강
  * 녹색
    * 파랑

+ 빨강
  + 녹색
    + 파랑

- 빨강
  - 녹색
    - 파랑

혼합해서 사용하는 것도 가능하다(내가 선호하는 방식)
```
* 1단계
    - 2단계
    	+ 3단계
            = 4단계
```

* 1단계
    - 2단계
    	+ 3단계
			= 4단계

## 2.4. 코드```<pre><code></code></pre>```
4개의 공백 또는 하나의 탭으로 들여쓰기를 만나면 변환되기 시작하여 들여쓰지 않은 행을 만날때까지 변환이 계속된다.

> 한줄 띄어쓰면 인식이 제대로 안되는 문제가 발생하곤 합니다.

```
This is a normal paragraph:

    This is a code block.
end code block.
```

<code>
```
This is a normal paragraph:
    This is a code block.
end code block.
```
</code>

실제로 적용해보면,
This is a normal paragraph:

    This is a code block.
end code block.

## 2.5. 수평선```<hr/>```
아래 줄은 모두 수평선을 만든다. 마크다운 문서를 미리보기로 출력할 때 *페이지 나누기* 용도로 많이 사용한다.
```
* * *

***

*****

- - -

---------------------------------------
```

* * *

***

*****

- - -

---------------------------------------


## 2.6. 링크
* 참조링크

```
[link keyword][id]
[id]: URL "Optional Title here"

Link: [Google][googlelink]
[googlelink]: https://google.com "Go google"
```

Link: [Google][googlelink]
[googlelink]: https://google.com "Go google"

* 인라인 링크
```
syntax: [Title](link)
```
Link: [Google](https://google.com, "google link")

* 자동연결
```
<http://example.com/>
<address@example.com>
```

<http://example.com/>
<address@example.com>

## 2.7. 강조
```
*single asterisks*
_single underscores_
**double asterisks**
__double underscores__
++underline++
~~cancelline~~
```
*single asterisks*
_single underscores_
**double asterisks**
__double underscores__
++underline++
~~cancelline~~
