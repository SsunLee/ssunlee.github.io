---
title: C# Thread 없이 Delay시키기      # 제목
layout: single                
author_profile: true          # 좌측 내 프로필 보여질 건지
read_time: true
comments: true                # 댓글 열것인지?
share: true                   # 공유 기능 
related: true
categories:                   # 카테고리 지정
- C#
tag:
- Delay, Csharp, Thread
toc: true                     # 목차 기능 
toc_sticky: true
toc_label: 목차  
description: C# 딜레이
meta_keywords: C# Delay
popular: true
---

#### 😀 Delay를 사용하게 된 계기

Thread.Sleep() 메서드로 일시 중단할 수 있지만,  
Sleep()이 되는 동안 자유롭게 컨트롤이 불가하고  
UI 화면에 보여지는 Delay를 주기 위해서 사용하기  
위해서는 비효율적이라고 판단이 되어서이다.


<br/>

#### 😀 Delay 구현하기
~~~cs
private static DateTime Delay(int MS)
{
    // Thread 와 Timer보다 효율 적으로 사용할 수 있음.
    DateTime ThisMoment = DateTime.Now;
    TimeSpan duration = new TimeSpan(0, 0, 0, 0, MS);
    DateTime AfterWards = ThisMoment.Add(duration);

    while (AfterWards >= ThisMoment)
    {
        System.Windows.Forms.Application.DoEvents();
        ThisMoment = DateTime.Now;
    }
    return DateTime.Now;
}
~~~

#### 😀 Delay 사용하기
~~~cs
private void test()
{
    // 테스트 
    for (i = 0; i<100;i++)
    {
        Diagnostics.Debug.print(i);
        Delay(500);
    }

}
~~~

#### 😀 Source Code
~~~cs
private void test()
{
    // 테스트 
    for (i = 0; i<100;i++)
    {
        Diagnostics.Debug.print(i);
        Delay(500);
    }

}


private static DateTime Delay(int MS)
{
    // Thread 와 Timer보다 효율 적으로 사용할 수 있음.
    DateTime ThisMoment = DateTime.Now;
    TimeSpan duration = new TimeSpan(0, 0, 0, 0, MS);
    DateTime AfterWards = ThisMoment.Add(duration);

    while (AfterWards >= ThisMoment)
    {
        System.Windows.Forms.Application.DoEvents();
        ThisMoment = DateTime.Now;
    }
    return DateTime.Now;
}
~~~

