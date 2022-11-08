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
![스크린샷 2022-11-08 오후 12 37 45](https://user-images.githubusercontent.com/88579497/200472051-d902a5c2-bf55-4c96-918b-e2db6be2fe05.png)

# index.html img를 수정하였다

## index.html 옆에 있는 M

은 Modified 라는 뜻으로 수정되었다 라는 뜻이 있다


<img width="1440" alt="스크린샷 2022-11-08 오후 12 41 18" src="https://user-images.githubusercontent.com/88579497/200472090-f6468fc2-838c-4201-9213-46e02b3d11b0.png">

오른쪽 fixed 된 bagge 부분을 수정하였다

![스크린샷 2022-11-08 오후 12 42 36](https://user-images.githubusercontent.com/88579497/200472198-1aae2bb8-993b-4ff8-a8fd-e98bcee45af9.png)


실제 터미널에 git status를 치면

index.html 이 수정되었다는 표시를 볼 수 있다


![스크린샷 2022-11-08 오후 12 46 59](https://user-images.githubusercontent.com/88579497/200472209-5851a633-01fb-4da1-8bce-0f16b74be9e4.png)


git add . 를 치고 확인 하면

초록색으로 변경되어 있는 것을 볼 수 있다

# 버전으로 만들기

![스크린샷 2022-11-08 오후 12.50.21.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1a1f027d-230f-4a39-adf5-3960e3d2373b/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2022-11-08_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_12.50.21.png)

git commit -m ‘문자’를 하고

git log로 확인 하면 위에 같이 master에 버전이 추가 되었음을 확인

![스크린샷 2022-11-08 오후 12 53 01](https://user-images.githubusercontent.com/88579497/200472308-510f2f95-ffd8-4d84-acbe-85ee80d2a178.png)


새롭게 파일을 추가해 보았고

U라는 단어가 나왔는데 이것은 Untracked file 이라는 뜻으로 새롭게 생성돼 추적하지 않은 파일이라는 뜻이다
