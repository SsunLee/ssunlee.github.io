---
title: 강좌 1장) C# Selenium 웹 자동화 (페이스북 활용예제)      # 제목
layout: single                
author_profile: true          # 좌측 내 프로필 보여질 건지
read_time: true
comments: true                # 댓글 열것인지?
share: true                   # 공유 기능 
related: true
categories:                   # 카테고리 지정
- C#
tag:
- Selenium, 자동화, 웹자동화
toc: true                     # 목차 기능 
toc_sticky: true
toc_label: 목차  
description: C# Selenium
meta_keywords: C# Selenium
popular: true
---

### **Selenium 이란?**
셀레늄(Selenium)은 웹 애플리케이션 테스트를 위한 포터블 프레임워크이다.  
 셀레늄은 테스트 스크립트 언어를 학습할 필요 없이   
 기능 테스트를 만들기 위한 플레이백 도구를 제공한다.   
 (셀례늄 IDE) C 샤프, 그루비, 자바, 펄, PHP, 파이썬, 루비, 스칼라 등   
 수많은 유명 프로그래밍 언어들에서 테스트를 작성하기 위한 테스트 도메인 특화 언어(Selenese)를 제공한다.   
 이 테스트들은 현대의 대부분의 웹 브라우저에서 수행이 가능하다.   
 셀레늄은 윈도우, 리눅스, macOS 플랫폼에서 디플로이된다.   
 아파치 2.0 라이선스로 배포되는 오픈 소스 소프트웨어이다.   
 웹 개발자는 무료로 다운로드, 사용할 수 있다.

<br/>

 ### **Visual Studio 시작**
Visual Studio 설치 부터 작성 하자 하면 너무 길어지니 그냥 세팅 되어있다는 간주하에 작성 해봅니다.  

 Visual Studio에는 Nuget Package라는 아주 좋은 기능이 있습니다.  
외부 라이브러리를 검색 후 설치까지 해주니 이게 웬 떡!  
원래는 dll을 다운받아서 일일이 Reference에 참조를 추가해주어야  
 했는데 많이 편합니다..

Nuget Package 받는 법은 아래 이미지와 같습니다.
![image](https://user-images.githubusercontent.com/41108401/122144940-55334280-ce8f-11eb-836d-91cdfff0d331.png)

<br/>

이미지와 같이 Nuget package 에서 Selenium을 검색하여  
다운로드 받으시면 끝입니다.

![image](https://user-images.githubusercontent.com/41108401/122145008-6bd99980-ce8f-11eb-9d9b-05d292946c77.png)

그럼 초기 세팅은 끝.


대충 form load Event에 코드를 작성 합니다.
Nuget으로 참조를 설정 했으니 사용할 때 아래 와같이 using 선언해줍니다.

~~~cs
using OpenQA.Selenium.Chrome;
using OpenQA.Selenium;
~~~
그 다음으로 Facebook을 띄워 봅니다.
~~~cs
private void Form1_Load(object sender, EventArgs e)
{
   IWebDriver driver = new ChromeDriver();
   driver.Navigate().GoToUrl("http://www.facebook.com");
}
~~~

끝. 참 쉽죠?.... 그냥 띄우는 것만 하면이지만요..
실행 후 화면은 아래와 같이 페이스북 화면이 딱! 나오네요.
![image](https://user-images.githubusercontent.com/41108401/122145176-b3f8bc00-ce8f-11eb-8bc9-5644bcd624a5.png)

다음 장에서는 이메일아디 입력, 비밀번호 입력, 로그인 하기까지 
작성 할 예정입니다.
