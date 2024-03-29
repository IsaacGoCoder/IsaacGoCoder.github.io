---
title: 마지막으로 생성,변경 된 객체 선택(Select Objects that Last Added Or Created)
date: 2024-03-29 14:53:58 +09:00
categories:
  - 프로젝트(Projects)
  - 오토리습|Autolisp(Projects)
tags:
  - autolisp
  - project
image: assets/img/background/cover;%20autolisp.png
---



### 기능(Functionality)
오토캐드에서 객체 선택시에 "p"키워드로 마지막으로 **선택**된 객체들은 선택할 수 있지만, 도면상 복사(copy), 클립보드복사(ctrl+c/v), 배열복사 등 마지막으로 생겨나거나 수정 된 객체들은 선택할 수 있는 방법이 없음

라이노3D에는, 마지막으로 생성되거나 변경 된 객체들을 선택할 수 있는 lastsel이라는 명령어가 있는데, 이와 유사한 기능을 개발함

이 리습으로는 다음과 같은 기능을 수행할 수 있음
1. 명령어, 리습으로 생성, 변경 된 객체들 선택
2. 클립보드로 붙여넣은 객체들 선택
3. 블럭 변경시 해당 블럭을 사용하는 모든 블럭참조들 선택


<br>
In AutoCAD, when selecting objects with the "p" keyword, the last **selected** objects are selected, but there is no built-in functionality to AutoCAD that select objects recently created or modified in the drawing (copy, ctrl+c/v, array copy, etc.) cannot be selected.

Rhino3D has a command "lastsel" that can select recently created or modified objects. I have developed similar functionality:

With this lisp, the following functions can be performed:

1. Select objects created or modified by command or lisp
2. Select objects pasted from clipboard
3. Select all block references using a block when the block is modified


<br>
<hr>

### 시연(Demonstration)
![](assets/img/attachment/sa_240217.gif)

1. Create - by Command
2. Move - by Command
3. Copy - by Command 
4. Array - by Command
5. Stratch - by Command
6. Paste - by Shortcut(Ctrl C + V)
7. Create & Modified - by Lisp