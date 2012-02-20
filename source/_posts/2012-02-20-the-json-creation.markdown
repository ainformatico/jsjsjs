---
layout: post
title: "the JSON creation"
date: 2012-02-20 23:19
comments: true
categories: [json]
author: Alejandro El Informático <a href="https://twitter.com/ainformatico">ainformatico</a>
---

devX wrote this to create a JSON:

``` javascript
var tmpJSON = '{"fileDate" : ", "fileSize" : 0,"fileUrl" : "' + jsonx.file + '"}';
LIB.imager.mycallbackData = jQuery.parseJSON(tmpJSON);
```
<!-- more -->

What's wrong here
----------------------
* use _jquery_ to create a _JSON_

How to conquer
----------------------

* create a _javascript_ object

``` javascript
LIB.imager.mycallbackData =
{
  fileDate : '',
  fileSize : 0,
  fileUrl  : jsonx.file
};
```
