---
layout: post
title: Protractor
date:   2015-09-02 15:30:31 +9:00 GMT
categories:
  - Javascript
tags:
  - AngularJS
  - protractor
---

## Protractor

##### Testing with Protractor

<pre class="prettyprint">
var thumbsUp = element(by.css('span.glyphicon-thumbs-up'));
var thumbsDown = element(by.css('span.glyphicon-thumbs-down'));

it('should check ng-show / ng-hide', function() {
  expect(thumbsUp.isDisplayed()).toBeFalsy();
  expect(thumbsDown.isDisplayed()).toBeTruthy();

  element(by.model('checked')).click();

  expect(thumbsUp.isDisplayed()).toBeTruthy();
  expect(thumbsDown.isDisplayed()).toBeFalsy();
});
</pre>

---
**참조**

* [AngrularJS testing framework : Protractor](https://github.com/angular/protractor){:target="_blank"}
