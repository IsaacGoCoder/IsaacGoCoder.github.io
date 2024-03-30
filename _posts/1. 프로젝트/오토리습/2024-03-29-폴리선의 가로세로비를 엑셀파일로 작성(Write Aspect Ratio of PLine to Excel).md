---
title: 폴리선의 가로세로비를 엑셀파일로 작성(Write Aspect Ratio of PLine to Excel)
date: 2024-03-29 13:54:05 +09:00
categories:
  - 1. 프로젝트(Projects)
  - 오토리습|Autolisp(Projects)
tags:
  - autolisp
  - project
  - excel
image: assets/img/attachment/rlOJu9G%20-%20Imgur.gif
---



### 기능(Functionality)

지정한 폴리선을 지정한 중심선 기준으로 좌우로 나누어 그 가로세로비를 엑셀에 작성

엑셀파일은 새 파일 생성 또는 기존파일에 추가가 가능하며, 기존파일에 추가시 가장 마지막에 입력 된 행의 아래에 정보가 추가 됨

한번에 여러개의 폴리선에 대한 정보 추가 가능

<br> 

Split the specified polyline into both sides based on the specified centerline and write their aspect ratios to Excel (not actually split that polyline)

The Excel file can be a new file or added from an existing file, and in the latter case, the information is added below the last row that has data.

The information of multiple polylines can be added at once

<br>
<hr>

### 시연(Demonstration)
![](assets/img/attachment/rlOJu9G%20-%20Imgur.gif)