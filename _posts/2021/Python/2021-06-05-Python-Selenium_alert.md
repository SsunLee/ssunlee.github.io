---
title: 파이썬 - Selenium IE Driver 팝업 처리  # 제목
layout: single                
author_profile: true          # 좌측 내 프로필 보여질 건지
read_time: true
comments: true                # 댓글 열것인지?
share: true                   # 공유 기능 
related: true
categories:                   # 카테고리 지정
- Python
tag:
- Python, Selenium, IEDriver
toc: true                     # 목차 기능 
toc_sticky: true
toc_label: 목차  
description: IEDriver 팝업 처리
meta_keywords: Python, Selenium, IEDriver
popular: true
---

### **🙋‍♂️ 들어가기 전**

IEDriver로 Selenium을 개발하는 중  
막히는 부분이 많았었는데
바로 '팝업'이 발생했을 때 처리하는 방법이었습니다.

물론 ChromeDriver에서도 동일하겠지만  
Switch_to_Alert()으로 처리 할 수 있습니다.

우선 '팝업'이 발생하면 엔터처리 하는 것 뿐만아니라  
팝업 내의 텍스트를 가져와 예외처리를 할 수 있을 것 같아  
팝업 내의 텍스트도 가져오는 방법도 작성 합니다.

![](https://images.velog.io/images/ssunbae/post/40be833d-872e-4077-a622-997bce37541d/image.png "팝업")

예를들어 Selenium으로 자동화를 하는 중 

비밀번호를 입력하라는 팝업  
아이디를 입력하라는 팝업
서버 오류가 있어서 발생하는 팝업   
등 예외처리를 할 때  
팝업 내의 텍스트로 if문 처리를 할 수 있을 것 같습니다.

<br/>

생각보다 간단한 방식으로 해결할 수 있었습니다.

### **🐯 팝업 내 TEXT 가져오기**

```Python
try:
    result = drv.switch_to_alert()
    print(result.text)
except:
    "popup : nothing"
```

위 와같이 drv.switch_to_aler()을 이용하여 처리하게 되는데  
팝업의 text를 위와 같이 출력할 수 있습니다.  

![](https://images.velog.io/images/ssunbae/post/77880b22-b701-4de7-965f-dcb88bd6e162/image.png "실행화면")  

<br/>


### **🐝 '팝업' 확인 및 닫기 하는 법**

```Python
try:
    result = drv.switch_to_alert()
    print(result.text)

    # Alert 창 확인
    result.accept()
    # Alert 창 닫기
    result.dismiss()

except:
    "popup : nothing"
```