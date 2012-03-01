---
layout: post
title: "Chaining like a boss"
date: 2012-03-01 16:00
comments: true
categories: [jquery]
author: Alejandro El Informático <a href="https://twitter.com/ainformatico">ainformatico</a>
---

_jquery_ chaining like a boss.

``` javascript
var actual = $(element).val();
$('.area' + actual + '').removeClass('ui-draggable-disabled');
$('.area' + actual + '').removeClass('ui-state-disabled');
$('.area' + actual + '').removeClass('ui-draggable');
$('.area' + actual + '').draggable(
{
  containment: "#canvas",
  start: function () {},
  stop: function () {}
});
$('.area' + actual + '').css(
{
  cursor: 'move',
  border: '1px solid white',
  background: 'red',
  opacity: .30
});
```
<!-- more -->

What's wrong here
----------------------
* not using the _jquery_ chaining
* bad use of `removeClass()`

How to conquer
----------------------
* use the _jquery_ chaining
* use `removeClass()` correctly
* cache the selector, _optional_

``` javascript
var actual  = $(element).val(),
    element = $('.area' + actual);
element
  .removeClass('ui-draggable-disabled ui-state-disabled ui-draggable')
  .draggable(
  {
    containment : "#canvas",
    start       : function () {},
    stop        : function () {}
  })
  .css(
  {
    cursor     : 'move',
    border     : '1px solid white',
    background : 'red',
    opacity    : .30
  });
```
