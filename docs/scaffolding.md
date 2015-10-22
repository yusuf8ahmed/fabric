---
layout: page
title: Scaffolding
---

Scaffolding refers to the global resets and dependencies that Palette is built upon.


## Recommended HTML boilerplate

If you're starting a new project, we recommend using the following boilerplate.

Palette makes use of certain HTML elements and CSS properties that **require** the use of the HTML5 doctype. Include it at the beginning of all your pages.

{% highlight html %}
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <title>Your page title</title>
    <meta name="description" content="Your page description">
  </head>
  <body>
    Your page body
  </body>
</html>
{% endhighlight %}

## Box-sizing

We reset `box-sizing` to `border-box` for every element in Palette. This allows us to more easily assign widths to elements that also have `padding` and `border`s.
