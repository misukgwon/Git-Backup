# Git CLI - Backup



## 1. 용어정리



### 1.1 용어

- 지역 저장소 (local repository) : 작업을 해서 버전을 생성하는 컴퓨터
- 원격 저장소 (remote repository) : 지역 저장소에서 작업을 끝낸 버전들을 업로드해서 지역 저장소와 똑같은 상태를 유지하는 컴퓨터에 설치되어 있는 저장소
- psuh :  지역 저장소에 있는 소스코드, 문서, 버전이 원격 저장소로 업로드
- clone :  원격 저장소의 내용을  또 다른 지역 저장소에 복제를 하는 과정
- pull : 다른 지역 저장소에서 원격 저장소로 push 된 내용을  원래의 저장소로 다운로드 하는 것



### 1.2 Git의 편리성

* 작업 이동성을 극대화



### 1.3 Git Hosting

- backup의 중심에 있는 원격 저장소 필요
- 직접 마련하기 어려우므로 이를 제공하는 서비스 이용, 이러한 서비스를 git hosting이라고 함



## 2. Git Hosting



### 2.1 Public Git hosting sites

| Provider                            | opn source | open source repsoitory | spce      | free private repository                    |
| ----------------------------------- | ---------- | ---------------------- | --------- | ------------------------------------------ |
| [GitHub](https://github.com/)       | No         | Free                   | unlimited | No                                         |
| [GitLab](https://about.gitlab.com/) | Yes        | Free                   | unlimited | Unlimited project, Unlimited collaboration |

- GitLab : 가격적인 측면에서 장점



## 3. 저장소 생성



1) 회원가입

2) 로그인

3) 새로운 저장소 생성 : Repositories - New

4) 저장소 이름 저장 및 상세 설명 기재

5)  Public : open source project

​     Private : 비공개 저장소, GitHub에서 비용 지불 필요

6) Create repository 버튼 클릭

7) 저장소 생성



## 4. 원격 저장소와 연결



1)  원격 저장소와 연결방법

- git remote add [원격 저장소 별명] [원격저장소 주소(연결방법은 HTTPS 방식을 체크한뒤)]

> ` git remote add origin https://github.com/misukgwon/Git-Backup.git` 

(원격 저장소가 여러 개 존재할 수 있으므로, 각각의 원격 저장소의 별명을 붙인다. 기본적인 원격 저장소는 origin이라는 이름을 관습적 으로 사용)



2) 원격 저장소 잘 연결됐는지 확인 방법

> `git remote`    

-> origin (화면에 출력)



3) 주소 확인

> `git remote -v`



## 5. Git Push



### 5.1 기본 원격 저장소 설정

> `git push --set-upstream origin master`

* 이후 git push만 입력해도 origin의 master라는 branch에 업로드

> ``Username for 'https://github.com' : ``
>
> ``Password for 'https://github.com' : ``

* ID와 PW 입력



### 5.1 업로드 방법

> `git add [파일]`
>
> `git commit -m '[message]'`



## 6. Git Clone



* 원격 저장소의 내용을 지역 저장소 2에 복제하는 것
* 여러 대의 컴퓨터에 같은 파일의 상태를 유지, 이동시 작업 가능

1) 저장소 주소 복사

2) `git clone [주소]`



## 7. Git Pull



- 지역 저장소 1로부터 원격 저장소로 push하여 새롭게 업로드 된 내용을 지역 저장소 2로 가져오는 방법

> `git pull`



## 8. Git과 오픈소스



* git 홈페이지 다운로드 화면에서 `Source Code` 클릭하면 GitHub로 연결됨
* open source를 git으로 다운받는 방법

> open source의 주소를 copy
>
> `git clone [주소입력]`





