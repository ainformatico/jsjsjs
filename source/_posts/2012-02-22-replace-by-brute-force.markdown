---
layout: post
title: "Replace by brute force"
date: 2012-02-22 17:22
comments: true
author: Alejandro El Informático <a href="https://twitter.com/ainformatico">ainformatico</a>
---

Replace all the matches!!!

``` javascript
for(var i = 0;i < str.length;i++)
{
  str = str.replace(/-/, '');
}
```
<!-- more -->

What's wrong here
----------------------
* use a loop to replace all the matches

How to conquer
----------------------

* use the `g` flag provided by the _regex_ engine

``` javascript
str.replace(/-/g, '');
```
