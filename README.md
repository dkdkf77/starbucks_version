# Starbucks Version 관리

<aside>
💡 깃 버전 관리 시스템(순서대로 진행)

# **개행 문자(New line)**

## **설정macOS**

$git config —global core.autocrlf input

## **Windows**

$git config —global core.autocrlf true

# **사용자 정보**

## **커밋(버전 생성)을 위한 정보 등록**

$git config —global [user.name](http://user.name/) ‘git 이름’

$git config --global user.email 'dkdkf312@gmail.com’

❗️ 되도록 git 이름과 git 이메일은 깃허브 아이디와 이메일을 사용해 주는게 좋다

# **구성 확인Q키를 눌러 종료!**

$git config —global —list

# 변경사항 추척 시작

$git init

현재 프로젝트에서 변경사항 추적(버전관리)을 시작

# 모든 파일 업로드

$git add .

모든 파일의 변경사항을 추적하도록 지정

일부 파일만 추적 하려면 $git add index.html

# 버전을 생성

$git commit -m ‘프로젝트 생성’

메시지(-m)와 함께 버전을 생성

버전을 생성 하였을때 → 새로운 파일을 생성하면 빨간색(변경된 파일이나 새로운 파일)

git add . 로 추가시 초록색으로 변경(변경 사항 추척)

commit으로 -m 추가 (새로운 버전 내역 추가)

# 원격 저장소 업로드

$git push origin master

origin이란 별칭의 원격 저장소로 버전 내역 전송

</aside>



# index.html img를 수정하였다
![스크린샷 2022-11-08 오후 12 37 45](https://user-images.githubusercontent.com/88579497/200472519-e26629e5-a1b8-4458-9581-d25c5850a41d.png)



## index.html 옆에 있는 M

은 Modified 라는 뜻으로 수정되었다 라는 뜻이 있다

<img width="1440" alt="스크린샷 2022-11-08 오후 12 41 18" src="https://user-images.githubusercontent.com/88579497/200472449-2d84a2cb-7c74-4c98-b69b-25545d468816.png">



오른쪽 fixed 된 bagge 부분을 수정하였다

![스크린샷 2022-11-08 오후 12 42 36](https://user-images.githubusercontent.com/88579497/200472198-1aae2bb8-993b-4ff8-a8fd-e98bcee45af9.png)


실제 터미널에 git status를 치면

index.html 이 수정되었다는 표시를 볼 수 있다


![스크린샷 2022-11-08 오후 12 46 59](https://user-images.githubusercontent.com/88579497/200472209-5851a633-01fb-4da1-8bce-0f16b74be9e4.png)


git add . 를 치고 확인 하면

초록색으로 변경되어 있는 것을 볼 수 있다

# 버전으로 만들기

![스크린샷 2022-11-08 오후 12 50 21](https://user-images.githubusercontent.com/88579497/200472367-f096e596-1922-49f9-8481-e78cca302b41.png)


git commit -m ‘문자’를 하고

git log로 확인 하면 위에 같이 master에 버전이 추가 되었음을 확인

![스크린샷 2022-11-08 오후 12 53 01](https://user-images.githubusercontent.com/88579497/200472308-510f2f95-ffd8-4d84-acbe-85ee80d2a178.png)


새롭게 파일을 추가해 보았고

U라는 단어가 나왔는데 이것은 Untracked file 이라는 뜻으로 새롭게 생성돼 추적하지 않은 파일이라는 뜻이다



## branch 로 login branch 버전 관리 및 merge


<aside>
💡 git branch 를 쓰면

현재 branch가 어디인지 알려주고  **현 branch master**

---

git branch -a를 쓰면 

브런치가 한개 만들어 진다 

remotes/origin/master

---

remotes= github 원격 저장소

origin = 저장소에 있는 origin 에 master

---

git branch signin → signin 이라는 branch를 만든다
![스크린샷 2022-11-09 오후 8 05 19](https://user-images.githubusercontent.com/88579497/200816320-aad83a52-1f55-47fe-a736-c1c291493618.png)
signin의 브랜취로 이동하려면 

git checkout signin  ⇒

Switched to branch 'signin’

master에서 → signin으로 바뀜 

---

signin 폴더를 만들고 폴더안에 index.html을 다시 만듬 

그러면 다시 git version 관리를 해줘야 하므로 

git staus, git add. git commit -m ‘버전 이름’

같은 명령어로 쳐주면 된다 

---

다시 git checkout master로 가게 되면 

signin 폴더와 index.html 파일이 없어지게 졌는데 

그 이유는 우리가 git add. 를 작업한 곳은 signin branch라서 

아직 merge를 하지 않아서 연결된 상태가 아닌 분리된 상태라는 것

---

보통 테스트가 다 끝나고 연결한다고 한다

</aside>

# git clone 

<aside>
💡 ls = mac 버전 현재 위치

dir = win 버전 현재 위치

cd .. ⇒ 한단계 올라가기

cd gitclone ⇒ 그 폴더로 이동

desktop 에서 git clone 레파지토리 복북

clone한 레파지토리 폴더 열기 

win 컨트롤 쉬프트 p 

mac 커멘드 쉬프트 p

검색창에 

쉘 명령 : PATH에 ‘code’ 명령 설치 

레파지토리 폴더에 접근 한 후 

cd starbucks_version 

code . ⇒ 새로운 창에 폴더 열기 

code . -r  ⇒ 현재 창에 폴더 열기

</aside>

<hr/>
<aside>
# git version 되돌리기 및 branch 관련 정보 


git reset --hard HEAD~되돌아갈 번호

HEAD = 최신 버전 에서 

~1  1번 뒤로 되돌리겠다 라는 의미 

git reset --hard ORIG_HEAD 

ORIG = origin  _ head

전 head로 리셋 시키는 명령어 컨트롤 Z 같은 명령어

# 다른 환경에서 clone으로 받은 후

없는 branch 로 이동하는 방법 

git branch -r 

git checkout -t origin/branch이름

## 가져 온 branch가 원하는 브랜치가 아닐때

git checkout master로 나간 다음

git branch -d branch 이름 ⇒ 지울 branch 입력

## branch를 생성하는 동시에 그 branch로 이동

git checkout -b 브랜치이름

</aside>
