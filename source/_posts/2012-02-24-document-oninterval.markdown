---
layout: post
title: "document oninterval"
date: 2012-02-24 16:44
comments: true
categories:
author: Alejandro El Informático <a href="https://twitter.com/ainformatico">ainformatico</a>
---

This is not as old as it seems.

Check if the _dom_ is fully loaded.

``` javascript From init.js
var init = setInterval(function()
{
  var element = document.getElementById('footer');
  if(element)
  {
    clearInterval(init);
    //actions
  }
}, 10);
```
<!-- more -->

What's wrong here
----------------------
* Use an interval tho check if the _dom_ is fully loaded

How to conquer
----------------------
* use the `onload` method from the `window` _object_

``` javascript
window.onload = function()
{
  //actions
};
```
