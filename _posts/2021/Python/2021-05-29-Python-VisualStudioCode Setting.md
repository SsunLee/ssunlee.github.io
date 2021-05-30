---
title: 비주얼스튜디오코드 - 파이썬 환경 설정   # 제목
layout: single                
author_profile: true          # 좌측 내 프로필 보여질 건지
read_time: true
comments: true                # 댓글 열것인지?
share: true                   # 공유 기능 
related: true
categories:                   # 카테고리 지정
- Python
tag:
- VisualStudioCode, Python
toc: true                     # 목차 기능 
toc_sticky: true
toc_label: 목차  
description: Visual Studio Code로 Python 실행하기 ^^
meta_keywords: VisualStudioCode, Python, 파이썬환경설정
popular: true
---



<br/>

## 🐝 Python 설치 하기
---

- 원하는 Version 으로 설치 합니다.  
저 같은 경우는 3.8 버전대를 다운로드 하였습니다.

<br/>

- Install 링크 ↓↓ (이미지를 클릭하면 이동 됩니다.)
[![image](https://user-images.githubusercontent.com/41108401/120063310-821ae380-c0a1-11eb-9410-48e5081f8f69.png)](https://www.python.org/downloads/)

<br/>

- 설치 파일로 설치를 하고 신경써야 할 부분은 경로 입니다.  
환경변수 설정이나 인터프리터 설정할 때 python 설치 경로를 알아야 하는데  
자동 생성되는 path는 잊어버리기 쉽기 때문입니다.
(저는 그냥 설치 했지만...)
![image](https://user-images.githubusercontent.com/41108401/120063625-189bd480-c0a3-11eb-9913-2c41ec873d98.png)

<br/>



<br/>

## 🦊 환경변수 설정 
---
[내 PC] 우클릭 -> [속성] - 좌측 [고급 시스템 설정] - 하단 [환경 변수(N)...] 선택

![image](https://user-images.githubusercontent.com/41108401/120063721-83e5a680-c0a3-11eb-8875-862115fdc040.png "환경변수")
환경변수 설정 후 제대로 설치되었는지 확인 합니다.  

![image](https://user-images.githubusercontent.com/41108401/120063732-965fe000-c0a3-11eb-8331-9c521b432e51.png "실행결과")

CMD 실행 시켜 python --version   입력하여 확인해봅니다.



<br/>

## 🐠 PIP 설치 확인 
---
pip install 로 여러가지 라이브러리를 다운로드할 수 있습니다.

이를 위해 최신버전이 설치되어있는지 미리 확인 합니다.

cmd를 실행시켜 아래와 같이 쳐봅니다.

```python
python -m pip install --upgrade pip
```
![image](https://user-images.githubusercontent.com/41108401/120063774-daeb7b80-c0a3-11eb-8cf2-c8b2cee6d2c1.png "실행결과")

---

<br/>

## 🦁 비주얼스튜디오코드 설치
아래의 링크를 접속하여 Visual Studio Code를 설치 합니다.  
- Install 링크 ↓↓ (이미지를 클릭하면 이동 됩니다.)
[![image](https://user-images.githubusercontent.com/41108401/120063986-f3a86100-c0a4-11eb-948e-17b5253e0730.png)](https://code.visualstudio.com/)

<br/><br/>

## 🦀 Python Extension 설치
---

- Step 1) 비주얼스튜디오코드의 좌측 아이콘을 눌러 'python'이라고 검색 후 Install 합니다.
![image](https://user-images.githubusercontent.com/41108401/120064020-2f432b00-c0a5-11eb-98bb-ac47ca01c099.png)

- Step 2) 저는 이미 설치가 되어 있기때문에 Uninstall로 보여지네요.
![image](https://user-images.githubusercontent.com/41108401/120064062-703b3f80-c0a5-11eb-91ed-771aedd50a5f.png)

<br/><br/>

## 🦋 Python Interpreter 선택
---

Visual Studio Code에서 Python을 사용하기 위해서는  
Pyhton이 Visual Studio Code의 
interpreter로 선택되어 있어야 합니다.

**Ctrl + Shift + P** 를 눌러 Select Interpreter 라고 검색 합니다.

![image](https://user-images.githubusercontent.com/41108401/120064144-d1fba980-c0a5-11eb-9c9d-da71dd5c1c30.png)

Python: Select Interpreter 를 선택해줍니다.

![image](https://user-images.githubusercontent.com/41108401/120064158-dcb63e80-c0a5-11eb-8656-2365f1ed16d4.png)

아래에 보이는 Python 을 선택 합니다.

만약, 보여지지 않는다면 직접 자신의 Python 설치 경로를 입력하면 됩니다.

<br/><br/>

## 🐳 간단한 코드 작성 후 실행
---

<br/>
모든 설정이 완료 되었다면 정말로 실행이 되는지 확인을 해보아야 합니다.

(1) Ctrl + N 을 눌러 New File을 만듭니다.  
(2) 파일을 저장하여 test.py 로 저장합니다.  
(3) 사진과 같이 코드를 작성 해봅니다.  
(4) 우측 상단의 ▷ 버튼으로 Run 해봅니다.

![image](https://user-images.githubusercontent.com/41108401/120064209-0e2f0a00-c0a6-11eb-8e84-86da0fd22b29.png)


<br/>

실행 결과 

![image](https://user-images.githubusercontent.com/41108401/120064333-96151400-c0a6-11eb-91a2-a10a53ffbc21.png)
