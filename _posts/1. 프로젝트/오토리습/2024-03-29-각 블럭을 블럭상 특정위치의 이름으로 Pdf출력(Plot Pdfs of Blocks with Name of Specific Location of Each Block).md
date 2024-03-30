---
title: 각 블럭을 블럭상 특정위치의 이름으로 Pdf출력(Plot Pdfs of Blocks with Name of Specific Location of Each Block)
date: 2024-03-29 14:39:10 +09:00
categories:
  - 1. 프로젝트(Projects)
  - 오토리습|Autolisp(Projects)
tags:
  - autolisp
  - project
  - plot
  - pdf
image: assets/img/attachment/PDFplot_240224.gif
---



### 기능(Functionality)

Pdf로 출력을 원하는 블록을 선택하고, 그 블록 내부에서 Pdf로 출력을 원하는 도면명이 있는 위치를 지정하면,
도면상에 동일한 블럭을 사용하는 모든 블럭참조객체들을 각 블럭참조의 각도를 따라서 해당 위치의 이름을 가지는 Pdf로 저장함

가로가 세로보다 길면 가로로, 세로가 더 길면 세로로 출력함

<br>
When a block to be ploted as Pdf is selected and a location of Text(the Pdf name) is specified within that block, plot all block reference objects using the same block in the drawing as Pdf with the name at the corresponding location of each block reference by its angle.

which means ifhorizontal size of the block reference is longer than its vertical size, it plots in landscape, otherwise in portrait.

<br>
<hr>

### 시연(Demonstration)
![](assets/img/attachment/PDFplot_240224.gif)