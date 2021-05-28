---
title: Git Command
layout: single
author_profile: true
read_time: true
comments: true
share: true
related: true
categories:
- Git
toc: true
toc_sticky: true
toc_label: 목차
description: 기본 
---


### 🐸 Git Clone
```
git clone https://github.com/SsunLee/ssunlee.github.io
```
---
<br/>

### 🐶 Remote 추가
```
 git remote add github https://github.com/SsunLee/ssunlee.github.io
```
---
<br/>

> **remote** : 원격 저장소와 연결하겠다.  
**add** : 원격 저장소를 추가 하겠다.  
**origin** : 원격 저장소의 origin이라는위치에 저장하겠다.
#### 실제 연결 되었는지 확인하고 싶을 때는 **git remote -v** 로 확인 가능 합니다.

---

<br/>

### 🐱 Github의 폴더 삭제
```python
git rm --cached -r unnessesary
```
---

<br/>

### 🐭 Github의 파일 삭제
```
git rm --cached -r unnessesary.xlsx 
```
---

<br/>

### 🐰 init 하기
```
git init 
```
내가 로컬에서 이 폴더를 git으로 사용하고자할 때 init 합니다.

---

<br/>

### 🦁 git add
```python
git add text.cs
```
하나의 특정한 파일을  추가 합니다.  
```
git add --all
```  
해당 폴더에 있는 모든 파일을 추가 합니다.

---

<br/>
<br/>

### 🦞 commit
```
git commit -m "불필요한 폴더 및 파일 삭제"
```
---

<br/>

### 🙉 push 
```
git push -u origin main
```
---