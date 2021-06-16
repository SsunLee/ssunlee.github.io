---
title: C# ListBox Selected Item 삭제하기 (Delete키)      # 제목
layout: single                
author_profile: true          # 좌측 내 프로필 보여질 건지
read_time: true
comments: true                # 댓글 열것인지?
share: true                   # 공유 기능 
related: true
categories:                   # 카테고리 지정
- C#
tag:
- ListBox, Selected, 삭제
toc: true                     # 목차 기능 
toc_sticky: true
toc_label: 목차  
description: C# ListBox Selected Item 삭제
meta_keywords: C# ListBox Selected Item 삭제
popular: true
---


### **😀 이 글을 작성하게 된 이유**

**ListBox** 라는 Control은 Winform에서 매우 많이 사용하는  
Control 중에 하나이다.  
간단하면서도 시인성이 좋아서 List를 뿌려줄 때도 많이들 사용한다.  
개발자가 이 Control을 처음 접할 때 가장 먼저 느끼는 점들은  
내가 생각했던 기능들이 **친절하게 모두 제공하지 않는다**는 것일 것이다.  

<br/>

예를 들면, 지금 이 글과 같은 기능일텐데  
당연하게 사용자는 리스트 하나를 선택해서 Delete 키를 누르면  
당연히 사라진다는 동작으로 알고 있을 것인데  
기본 Control에서 그런기능은 제공하지 않는다.  
결국은 직접 구현을 해두어야 한다는 것이다.  
그래서 이렇게 의미가 있을지는 모르지만  
까먹지 않도록? 나중에 복사 붙여넣으려는 목적으로 
여기 Blog에 작성을 해봅니다.

<br/><br/>

### **😀 구현 방법**
ListBox에서 Item을 선택을 한 상태에서 Delete 키를 눌러야 하기때문에  
ListBox에서 KeyDown Event로 받아서 처리를 합니다.  
KeyEvent가 들어오게 되었을 때, 
KeyCode가 Delete 인지 Check를 한 후 item을 지워주면 될 것입니다. 

<br/><br/>

### **😀 Srouce Code**

~~~cs
private void lst_files_KeyDown(object sender, KeyEventArgs e)
{
    if (e.KeyCode == Keys.Delete)
    {
        //delete
        ((ListBox)sender).Items.RemoveAt(((ListBox)sender).SelectedIndex);
    }
}
~~~
sender로 받아 들여진 object를 ListBox로 변환을 하여,  
현재 선택 된 SelectedIndex라는 Property를 통해서 선택한 항목을 Remove 합니다.

![image](https://user-images.githubusercontent.com/41108401/122157521-f0cfad80-cea5-11eb-82a2-d061bbee1f9e.png)