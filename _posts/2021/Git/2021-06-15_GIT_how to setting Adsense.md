---
title: Github 블로그에 에드센스 광고 넣기  # 제목
layout: single                
author_profile: true          # 좌측 내 프로필 보여질 건지
read_time: true
comments: true                # 댓글 열것인지?
share: true                   # 공유 기능 
related: true
categories:                   # 카테고리 지정
- github, 애드센스, 광고
tag:
- github, adsens, 광고, 애드센스
toc: true                     # 목차 기능 
toc_sticky: true
toc_label: 목차  
description: 광고 달기
meta_keywords: 광고달기
popular: true
---



### 😀 에드센스 사이트 추가 하기

```javaScript
<script data-ad-client="ca-pub-3025305005440839" async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
```
에드센스 홈페이지에서 신청을 하면 위와 같은 스크립트 코드를 제공해줍니다.
해당 스크립트를 복사해서 내 github blog에 뿌려줄 것 입니다.

<br/>

### 😀 하단 footer 영역에 추가
_layout\default.html 에 추가 합니다.
```javascript
<section class="page__content" itemprop="text">

</section>

<script data-ad-client="ca-pub-3025305005440839" async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>

<footer class="page__meta">

</footer>
```

### 😀 블로그 하단에 추가
_layout\default.html 에 작성 (위에서 이미 함)

_include\footer\custom.html 에 작성
```js
<!-- start custom footer snippets -->
<script data-ad-client="ca-pub-3025305005440839" async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
<!-- end custom footer snippets -->
```


### 😀 각 포스트 하단에 추가
_layout\single.html 에 작성
```js
      <script data-ad-client="ca-pub-3025305005440839" async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>

      <section class="page__content">

      </section>

      <script data-ad-client="ca-pub-3025305005440839" async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
```
