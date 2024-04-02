---
title: 폴리선 내부의 특정문자객체를 엑셀에 작성(Write Excel File From Text Objects Included by Polyline)
date: 2024-04-02 21:34:10 +09:00
categories:
  - 1. 프로젝트(Projects)
  - 오토리습|Autolisp(Projects)
tags:
  - autolisp
  - project
  - excel
  - include
  - polyline
public_post: true
image: assets/img/attachment/tox_240402.gif
---

### 기능(Functionality)

폴리라인을 선택하면, 선택한 폴리라인 내부에 존재하는 문자객체 중 " "(띄어쓰기 한칸)이 포함된 문자객체들만 선택하여, 해당 띄어쓰기를 기준으로 왼쪽과 오른쪽의 데이터를 각각 엑셀의 A열과 B열에 작성

<br>
Once a Polyline selected, it finds all Text objects, whose contents contain " "(a single space), then open a new excel sheet and write datas that seperated by " " in columns A and B

<br>
<hr>

### 시연(Demonstration)
![](assets/img/attachment/tox_240402.gif)