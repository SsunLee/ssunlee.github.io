---
title: Ruby 설치 및 환경 설정  # 제목
layout: single                
author_profile: true          # 좌측 내 프로필 보여질 건지
read_time: true
comments: true                # 댓글 열것인지?
share: true                   # 공유 기능 
related: true
categories:                   # 카테고리 지정
- Git
toc: true                     # 목차 기능 
toc_sticky: true
toc_label: 목차
description: 기본 
---


🐶 Ruby 설치 및 환경 설정
========================
<br/>
<br/>
<br/>
<br/>
<br/>


## 🦁 Ruby 설치
---
<br/>

ㆍ Click : [Ruby Install ](https://rubyinstaller.org/downloads/)  


> **Ruby 설치 이유 :**  
 동적 객체 지향 스크립트 프로그래밍 언어인 Ruby로 작성되었기 때문에  
 로컬 개발 환경 세팅을 위해서는 Rubby 설치가 필요합니다.

<br/>

![](https://images.velog.io/images/ssunbae/post/f7f6ecfa-d0b3-4fe6-ba10-a3f70eb815c1/image.png)

~~저는 Ruby+Devkit 3.0 1-1 (x64) 를 다운 받았습니다.~~  
다른 버전은 오류가나서 Ruby+Devkit 2.5.7-1 (x64) 로 설치 합니다.

![](https://images.velog.io/images/ssunbae/post/ff58da45-af10-4f21-aff8-a52dd8cfbde1/image.png)

![](https://images.velog.io/images/ssunbae/post/349a19fc-8af9-4fa5-a3a8-7cdee271dd49/image.png)

![](https://images.velog.io/images/ssunbae/post/f6c8b9a5-3a95-4909-8455-6ae66d9ff95b/image.png)


Ruby를 설치 완료 하면 이렇게 화면이 뜨는 걸 확인 합니다.
![](https://images.velog.io/images/ssunbae/post/b31b364f-bf30-4183-86f7-761b16b20051/image.png)


Gemfile이 있는 경로에서 명령어를 실행하기 위해  
file이 있는 경로에서 cmd라고 검색을 합니다.

![](https://images.velog.io/images/ssunbae/post/daada190-7707-4e0a-832f-fe59e775d2a1/image.png)

```
gem install bundler
bundle
jekyll serve
```
![](https://images.velog.io/images/ssunbae/post/065487e3-c616-47b7-a333-e9ee5bb0f772/image.png)
<br/>
<br/>
<br/>
<br/>

## 🦁 Ruby 설치 확인  
---
<br/>

이미지와 같이 명령어가 잘 실행이 되면  

인터넷 주소 창에 **http://localhost:4000/** 를 입력하면 아래와 같이 sample 사이트가 보여집니다.

![](https://images.velog.io/images/ssunbae/post/4b923614-823f-49be-8f39-c1e56873de38/image.png)

<br/>

최종 push 하기 전 작업 
불필요한 파일을 정리하는 작업을 합니다.

```
.github
test
.editorconfig
.gitattributes
.travis.yml
CHANGELOG.md
docs(샘플 파일들이 들어가 있는 폴더)
```
저는 폴더에서 직접 지웠습니다. 

<br/>



## 🦁 폴더에 업로드 된 내용 PUSH 
---

push를 해보겠습니다.
```
git add --all
git commit -m "First Upload"
git push -u origin main 
```

> **Trouble Shooting**

- 아래와 같은 오류가 발생하는 경우 해결법을 실행 후 다시 push

```
tnsqo@DESKTOP-FK3U9VS MINGW64 /c/sun/sunbae_blog (main)
$ git push -u origin main
To https://github.com/SsunLee/ssunlee.github.io.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/SsunLee/ssunlee.github.io.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

- 해결법 :  git pull origin 브런치명 --allow-unrelated-histories

```
tnsqo@DESKTOP-FK3U9VS MINGW64 /c/sun/sunbae_blog (main)
$ git pull origin main  --allow-unrelated-histories
From https://github.com/SsunLee/ssunlee.github.io
 * branch            main       -> FETCH_HEAD
CONFLICT (add/add): Merge conflict in README.md
Auto-merging README.md
Automatic merge failed; fix conflicts and then commit the result.
```

<br/>
<br/>



PUSH 가 제대로 되었다면 내 github 주소에 접속할 때도 동일하게
표시되는 것을 확인 할 수 있습니다.
![](https://images.velog.io/images/ssunbae/post/36cacd39-4920-4a70-b3e6-eb5264b3b0d4/image.png)

<br/><br/>

## 🦁 Ruby Server 실행방법
---

```
gem install bundler
bundle
jekyll serve
```
또는
```
bundle exec jekyll serve
```


> 블로그 게시물 작성은 네이밍 룰에 맞게  
YEAR-MONTH-DAY-title.md 라고 합니다.  
양식에 맞게 .md 파일을 생성하면 자동으로 뜨는지 보아야 겠습니다.