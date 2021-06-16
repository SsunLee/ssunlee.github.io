---
title: Python 약수 구하기 (간단예제)     # 제목
layout: single                
author_profile: true          # 좌측 내 프로필 보여질 건지
read_time: true
comments: true                # 댓글 열것인지?
share: true                   # 공유 기능 
related: true
categories:                   # 카테고리 지정
- Pyhton
tag:
- aliquot, 약수
toc: true                     # 목차 기능 
toc_sticky: true
toc_label: 목차  
description: 약수 구하기
meta_keywords: 약수 구하기
popular: true
---

### 😀 약수란?

b=an인 정수 n이 존재할 때, a|b라 하고, 이때의 a를 b의 약수라 한다.  
모든 자연수는 최소한 1과 자기 자신을 약수로 갖는다.  
1과 자기 자신밖에 약수가 존재하지 않는  
1보다 큰 자연수를 소수(素數)라고 한다.  
소원, 즉 소수의 진정한 정의는 이곳에 있다.  
[[출처 : 나무위키]](https://namu.wiki/w/%EC%95%BD%EC%88%98(%EC%88%98%ED%95%99))

<br/>

### 😀 약수 구하는 법
우선 약수를 구하는 방법은  
n 을 나누었을 때 나머지가 0인 것을 약수라 한다.  
예를 들어 20 의 약수라 하면  
20 % 1 == 0  
20을 1로 나눈 나머지가 0인 경우 약수이다.

![image](https://user-images.githubusercontent.com/41108401/122141340-0fbf4700-ce88-11eb-80e4-8ab978052e55.png)

<br/>

### 😀 약수 구하는 코드 짜기
먼저 약수를 구하기 위해 입력 받은 수까지 반복문을 돌립니다.  

여기서 num+1 을 하는 이유는 1 부터 20보다 작을 때까지이니 20은 반복하지 않기 때문에 +1을 해줍니다
```Python
for i in range(1, num+1):
```
if문으로 20 % 1 == 0 인지 체크를 하고 약수인지 판단을 합니다.

이런 방식으로 코드를 짜면 아래와 같이 나올 수 있습니다.
```Python
num = int(input("수? "))

for i in range(1, num+1):
    if num % i == 0:
        # 약수임
        print(i, end=' ')
print()
```