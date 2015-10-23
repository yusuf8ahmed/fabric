---
layout: page
title: Layout
---

The layout includes basic page containers and a responsive, 12-column grid system.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Container

Center your page's contents with a `.container`.

{% highlight html %}
<div class="container">
  <!-- contents here -->
</div>
{% endhighlight %}

The container applies `width: 1240px;` and uses horizontal `margin`s to center it.

## Grid

### How it works

The grid is pretty standard — you create rows with `.row-md` or `.row-lg` and individual columns with a `.col-*` class. Here's how it works:

- Add a `.container` to encapsulate everything and provide ample horizontal gutter space.
- Create your outer row to clear the floated columns with `<div class="row-md">` or `<div class="row-lg">`.
- Add your columns with individual `<div class="row-...">`s.

### Demo

In practice, your columns will look like the example below.

{% example html %}
<div class="container">
  <div class="row-md">
    <div class="col-2">
      .col-1
    </div>
    <div class="col-10">
      .col-11
    </div>
  </div>

  <div class="row-md">
    <div class="col-6">
      .col-6
    </div>
    <div class="col-6">
      .col-6
    </div>
  </div>

  <div class="row-md">
    <div class="col-8">
      .col-8
    </div>
    <div class="col-4">
      .col-4
    </div>
  </div>
</div>
{% endexample %}

### Containers

Besides the standard `.container`, you can also use:

- `.container-fluid` for a fullwidth container
- `.container-padded` for a `.container` that has padding on either side
- `.container-yellow` and `.container-gray` for colored containers

{% example html %}
<div class="container-padded container-yellow">
  <p>
    .container-padded .container-yellow
  </p>
</div>
{% endexample %}
