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

## 2.1 마크다운이란?
>[**Markdown**]은 텍스트 기반의 마크업언어로 2004년 존그루버에 의해 만들어졌으며 쉽게 쓰고 읽을 수 있으며 HTML로 변환이 가능합니다. 특수기호와 문자>를 이용한 매우 간단한 구조의 문법을 사용하여 웹에서도 보다 빠르게 컨텐츠를 작성하고 보다 직관적으로 인식할 수 있습니다.
>마크다운이 최근 각광받기 시작한 이유는 깃헙([https://github.com](https://github.com)) 덕분입니다. 깃헙의 저장소Repository에 관한 정보를 기록하는 >README.md는 깃헙을 사용하는 사람이라면 누구나 가장 먼저 접하게 되는 마크다운 문서였습니다. 마크다운을 통해서 설치방법, 소스코드 설명, 이슈 등을 간단>>하게 기록하고 가독성을 높일 수 있다는 강점이 부각되면서 점점 여러 곳으로 퍼져가게 됩니다.

## 2.2. 마크다운의 장-단점
### 2.2.1. 장점
	$ 간결합니다.
	$ 별도의 도구없이 작성가능합니다.
	$ 다양한 형태로 변환이 가능합니다.
	$ 텍스트(Text)로 저장되기 때문에 용량이 적어 보관이 용이합니다.
	$ 텍스트파일이기 때문에 버전관리시스템을 이용하여 변경이력을 관리할 수 있습니다.
	$ 지원하는 프로그램과 플랫폼이 다양합니다.
### 2.2.2. 단점
	$ 표준이 없습니다.
	$ 표준이 없기 때문에 도구에 따라서 변환방식이나 생성물이 다릅니다.
	$ 모든 HTML 마크업을 대신하지 못합니다.

## 2.3 마크다운 사용법(문법)
### 2.3.1 헤더Headers
* 큰제목: 문서 제목
    ```
    Heading
    =============
    ```
    Heading
    =============

* 작은제목: 문서 부제목
    ```
    Heading
    -------------
    ```
    Heading
    -------------

* 글머리: 1~6까지만 지원
```
# Heading1
## Heading2
### Heading3
#### Heading4
##### Heading5
###### Heading6
```
# Heading1
## Heading2
### Heading3
#### Heading4
##### Heading5
###### Heading6
####### Heading7

### 2.3.2 BlockQuote
이메일에서 사용하는 ```>``` 블럭인용문자를 이용한다.
```
> Lorem ipsum dolor sit amet
```
> Lorem ipsum dolor sit amet
>	> Lorem ipsum dolor sit amet
>	>	> Lorem ipsum dolor sit amet

이 안에서는 다른 마크다운 요소를 포함할 수 있다.
> ### Heading
> * List
>	```
>	code
>	```

### 2.3.3 목록
#### ● 순서있는 목록(번호)
순서있는 목록은 숫자와 점을 사용한다.
```
1. First
2. Second
3. Third
```
1. First
2. Second
3. Third

**현재까지는 어떤 번호를 입력해도 순서는 내림차순으로 정의된다.**
```
1. 첫번째
3. 세번째
2. 두번째
```
1. 첫번째
3. 세번째
2. 두번째

#### ● 순서없는 목록(Unordered List)
```*``` 또는 ```-```를 사용해서 순서가 없는 리스트를 작성할 수 있습니다. 
tab 또는 2칸 띄어쓰기를 통해 중첩된 항목을 작성할 수 있습니다.
```
* red
  * green
    * blue

+ red
  + green
    + blue

- red
  - green
    - blue
```
* red
  * green
    * blue

+ red
  + green
    + blue

- red
  - green
    - blue
    
### 2.3.4 코드블럭(Code blocks)
코드블럭은 일반 문장 사이에 단어, 짧은 문장 단위로 표현할 수 있는 방법과 여러줄의 코드를 삽입하는 방법이 있습니다.

> 단어, 한줄의 코드를 감싸는 경우 `를 감쌉니다.

```
마크다운은 코드블럭을 `<pre>`와 `<code>`로 감쌉니다.
```

마크다운은 코드블럭을 ```<pre>```와 ```<code>```로 감쌉니다.

여러줄의 코드를 나타내는 코드블럭의 경우 코드블럭의 시작과 끝을 
'''으로 감싸고 내부에 코드를 작성하면 됩니다.

```
fucntion square(n) {
  return n * n;
}
```


### 2.3.5 수평선(Horizontal Rules)
문단과 문단 사이를 나눌 때 등 사용되는 수평선은 HTML의 ```<hr />```과 같이 동작합니다.
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


### 2.3.6 링크
HTML의 하이퍼링크와 같은 링크는 다음과 같이 작성합니다. title은
생략이 가능합니다.

* 참조링크
```
[example](http://example.com "title")

검색엔진은 [구글](https://www.google.com "구글")을 사용합니다.
```
[example](http://example.com "title")

검색엔진은 [구글](https://www.google.com "구글")을 사용합니다.

* 자동연결
```
<http://github.com/>
<address@example.com>
```

<http://github.com/>
<address@example.com>

### 2.3.7 강조
HTML의 ```<em>```과 같은 동작을 하는 강조는 ```*```, ```_```가 있고
```<strong>```은 ```**```와 ```__```를 사용합니다. 취소선은 ```~~```을 사용합니다.
```
*강조*한 텍스트
_강조_한 텍스트
```
*강조*한 텍스트

```
**강조**한 텍스트
__강조__한 텍스트
```
**강조**한 텍스트

```
~~취소~~한 텍스트
```

~~취소~~한 

### 2.3.8 이미지 삽입(Images)
이미지는 역시 HTML의 ```<img>```태그와 동일하게 작동합니다. 대체
텍스트를 삽입할 수 있으며, 링크 또는 로컬의 이미지파일을 연결할 수 있습니다.
```
![대체 텍스트](/경로/example.jpg)
![대체 텍스트](링크)
```
```
![Github](./public/img/3/github.png)
```
![github-mark](https://cdn-images-1.medium.com/max/1200/1*dDNpLKu_oTLzStsDTnkJ-g.png)
```
![github-mark](https://cdn-images-1.medium.com/max/1200/1*dDNpLKu_oTLzStsDTnkJ-g.png)
```
![github-mark](https://cdn-images-1.medium.com/max/1200/1*dDNpLKu_oTLzStsDTnkJ-g.png)

사이즈 조절 기능은 없기 때문에 ```<img width="" height=""></img>```를 이용한다.


