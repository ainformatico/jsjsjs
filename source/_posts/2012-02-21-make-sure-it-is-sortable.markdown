---
layout: post
title: "Make sure it is sortable"
date: 2012-02-21 19:13
comments: true
categories: [jqueryui]
author: Alejandro El Informático <a href="https://twitter.com/ainformatico">ainformatico</a>
---

devX: Make it sortable!!!

``` javascript
//$("#demo") is the same as $(this).next()
$(this).next().sortable('enable');
$(this).next().fadeIn('fast', function (e) {
    $("#demo").sortable('enable');
});
```
<!-- more -->

What's wrong here
----------------------
* set `$('#demo')` as `sortable` twice

How to conquer
----------------------
* remove the first `sortable` statement
* cache `$("#demo")` into a variable

``` javascript
var item = $("#demo");
item.fadeIn('fast', function()
{
  item.sortable('enable');
});
```
