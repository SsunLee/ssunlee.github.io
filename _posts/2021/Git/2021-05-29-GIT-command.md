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
toc_label: ๋ชฉ์ฐจ
description: ๊ธฐ๋ณธ 
---


### ๐ธ Git Clone
```
git clone https://github.com/SsunLee/ssunlee.github.io
```
---
<br/>

### ๐ถ Remote ์ถ๊ฐ
```
 git remote add github https://github.com/SsunLee/ssunlee.github.io
```
---
<br/>

> **remote** : ์๊ฒฉ ์ ์ฅ์์ ์ฐ๊ฒฐํ๊ฒ ๋ค.  
**add** : ์๊ฒฉ ์ ์ฅ์๋ฅผ ์ถ๊ฐ ํ๊ฒ ๋ค.  
**origin** : ์๊ฒฉ ์ ์ฅ์์ origin์ด๋ผ๋์์น์ ์ ์ฅํ๊ฒ ๋ค.
#### ์ค์  ์ฐ๊ฒฐ ๋์๋์ง ํ์ธํ๊ณ  ์ถ์ ๋๋ **git remote -v** ๋ก ํ์ธ ๊ฐ๋ฅ ํฉ๋๋ค.

---

<br/>

### ๐ฑ Github์ ํด๋ ์ญ์ 
```python
git rm --cached -r unnessesary
```
---

<br/>

### ๐ญ Github์ ํ์ผ ์ญ์ 
```
git rm --cached -r unnessesary.xlsx 
```
---

<br/>

### ๐ฐ init ํ๊ธฐ
```
git init 
```
๋ด๊ฐ ๋ก์ปฌ์์ ์ด ํด๋๋ฅผ git์ผ๋ก ์ฌ์ฉํ๊ณ ์ํ  ๋ init ํฉ๋๋ค.

---

<br/>

### ๐ฆ git add
```python
git add text.cs
```
ํ๋์ ํน์ ํ ํ์ผ์  ์ถ๊ฐ ํฉ๋๋ค.  
```
git add --all
```  
ํด๋น ํด๋์ ์๋ ๋ชจ๋  ํ์ผ์ ์ถ๊ฐ ํฉ๋๋ค.

---

<br/>
<br/>

### ๐ฆ commit
```
git commit -m "๋ถํ์ํ ํด๋ ๋ฐ ํ์ผ ์ญ์ "
```
---

<br/>

### ๐ push 
```
git push -u origin main
```
---