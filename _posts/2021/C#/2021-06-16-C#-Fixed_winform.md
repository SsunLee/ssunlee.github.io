---
title: C# 창 Size 조절 못하게 막기      # 제목
layout: single                
author_profile: true          # 좌측 내 프로필 보여질 건지
read_time: true
comments: true                # 댓글 열것인지?
share: true                   # 공유 기능 
related: true
categories:                   # 카테고리 지정
- C#
tag:
- Form, Size
toc: true                     # 목차 기능 
toc_sticky: true
toc_label: 목차  
description: C# 윈폼 창크기 고정하기
meta_keywords: C# 윈폼 창크기 고정하기
popular: true
---


### **😀 방법 1**
AutoSizeMode를 GrowAndShrink 로 변경 하면 된다.

![image](https://user-images.githubusercontent.com/41108401/122157730-54f27180-cea6-11eb-9ca6-f2499aadac3a.png)

<br/><br/>

### **😀 방법2**
FormBorderStyle - FixedSingle 바꾸기

![image](https://user-images.githubusercontent.com/41108401/122157786-6cc9f580-cea6-11eb-9746-a865d034ecd0.png)


<br/><br/>

### **😀 방법3**
코드로 사이즈 정해두기
~~~cs
this.MinimumSize = new Size(140, 480);
this.MaximumSize = new Size(140, 480);
~~~