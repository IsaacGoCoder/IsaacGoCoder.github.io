---
title: <% tp.file.title %>
date: <% tp.date.now("YYYY-MM-DD HH:mm:ss +09:00") %>
categories:
  - 오토리습
  - 오토리습배우기
tags:
  - autolisp
  - learning
image: assets/img/background/cover;%20autolisp.png
---
<% await tp.file.rename(tp.date.now("YYYY-MM-DD") + "-" + tp.file.title) %>