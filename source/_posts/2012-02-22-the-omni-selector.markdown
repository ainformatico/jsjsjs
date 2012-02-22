---
layout: post
title: "The omni selector"
date: 2012-02-22 16:32
comments: true
categories: [selector, jquery]
author: Alejandro El Informático <a href="https://twitter.com/ainformatico">ainformatico</a>
---

devX: Why to use _jquery_ if you can do it with browser _API_. Oh, wait! _jquery_ can do it too?. So let's use both! Why not?

``` javascript
var myurl = document.getElementById("captureUrl").value;
//5 lines below
var data = $("#captureUrl").val();
```
<!-- more -->

What's wrong here
----------------------
* Use two different ways to get the same data

How to conquer
----------------------
* use the same selector

``` javascript
var myurl = data = $("#captureUrl").val();
```
