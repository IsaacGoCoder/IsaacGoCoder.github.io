---
title: <% tp.file.title %>
date: <% tp.date.now("YYYY-MM-DD HH:mm:ss +09:00") %>
categories:
  - 코딩
  - Swift
tags:
  - swift
image: assets/img/attachment/코딩-Swift.png
---
<% await tp.file.rename(tp.date.now("YYYY-MM-DD") + "-" + tp.file.title) %>