---
layout: page
title: Scaffolding
---

Scaffolding refers to the global resets and dependencies that Palette is built upon.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## HTML5 doctype

Palette makes use of certain HTML elements and CSS properties that **require** the use of the HTML5 doctype. Include it at the beginning of all your pages.

{% highlight html %}
<!DOCTYPE html>
<html>
  ...
</html>
{% endhighlight %}

## Box-sizing

We reset `box-sizing` to `border-box` for every element in Palette. This allows us to more easily assign widths to elements that also have `padding` and `border`s.
