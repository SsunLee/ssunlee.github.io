---
title: 강좌 2장) C# Selenium 웹 자동화 (페이스북 로그인하기)      # 제목
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

### **들어가기 전**

C# Selenium Visual Studio
시간을 내어 2장을 시작하도록 합니다.

1장에서는 ChromDriver 연결 후 GoToUrl을 사용하여 Facebook 창을 켜는 것 까지 했습니다.

목적은 '로그인' 하는 것이니 로그인에 필요한
이메일, 비밀번호를 입력 하는 것을 해보겠습니다.

<br/>

#### **😀 로그인 아이디 입력하기!**

우선 값을 텍스트 상자에 넣으려면 저 텍스트 상자를 찾아야 하겠죠?
방법은 간단합니다.
이메일을 입력할 텍스트 상자의 id 값을 찾으면 됩니다.  
![image](https://user-images.githubusercontent.com/41108401/122145422-2e294080-ce90-11eb-9637-62ee0f892b6a.png)

~~~cs
var element = driver.FindElement(By.Name("email"));
~~~

저 위에 텍스트 상자 id가 email 인지 어떻게 아냐구요?  
크롬 개발자 모드를 켜서 확인 하면 됩니다.

![image](https://user-images.githubusercontent.com/41108401/122145478-45682e00-ce90-11eb-8320-f49586f4ad46.png)

그럼 아래와 같은 화면이 뜨는데 버튼을 가르키고 있는 부분의 id를 확인 하면 됩니다.

![image](https://user-images.githubusercontent.com/41108401/122145497-5022c300-ce90-11eb-9d95-8cd222616f88.png)

보일 지 모르겠지만 자세히 보면 id 부분을 찾을 수 있습니다.
![image](https://user-images.githubusercontent.com/41108401/122145527-603aa280-ce90-11eb-8d02-03178368efcb.png)

그리하여 최종 코드는 아래 처럼 하면 되겠습니다.

~~~cs
var element = driver.FindElement(By.Name("email"));
string email = "adcde@gmail.com";
element.SendKeys(email);
~~~
코드를 실행하면 해당 박스에 내용이 입력 되겠죠.  
![image](https://user-images.githubusercontent.com/41108401/122145579-75afcc80-ce90-11eb-9163-fd7efb7e234e.png)

<br/>

#### **😀 로그인 비밀번호 입력하기!**
이메일 텍스트 상자의 id를 찾았을 때와 동일한 방법으로  
찾으면 됩니다.
~~~cs
element = driver.FindElement(By.Name("pass"));
string pass = "qwer1234";
element.SendKeys(pass);
~~~
![image](https://user-images.githubusercontent.com/41108401/122145627-92e49b00-ce90-11eb-9666-42229ba29732.png)


<br/>

#### **😀 로그인 버튼 누르기!**

~~~cs
element = driver.FindElement(By.Name("pass"));
string pass = "qwer1234";
element.SendKeys(pass);
element.Submit();
~~~
물론 기존 방식 처럼 할 수도 있습니다.  

![image](https://user-images.githubusercontent.com/41108401/122145723-be678580-ce90-11eb-9ed1-bd57492e82a1.png)

~~~cs
element = driver.FindElement(By.Id("u_0_3"));       
// Facebook Login Submit Button
element.Click();
~~~

위에서는 단순히 FindElement(By.Name.... 으로 Element를 찾았지만 
다양하게 Element를 찾아서 지정해 줄 수 있습니다.

![image](https://user-images.githubusercontent.com/41108401/122145781-db9c5400-ce90-11eb-8313-c138d18e07e9.png)

자세한 가이드는 아래 사이트 참조하면 될 것 같아요.
엄청 자세하게 나와있네요.

그럼 일단은 여기까지...

다음엔 아래 형식 으로 된 것을
~~~html
<Span> dddd </Span>
~~~
찾는 것도 해볼 예정 입니다.

<br/>
<br/>

#### **😀참조 링크**

 ToolsQA : [[Link]](http://toolsqa.com/selenium-webdriver/findelement-and-findelements-command/)