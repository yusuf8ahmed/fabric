---
layout: page
title: Layout
---

The layout includes page containers and a responsive, 12-column grid system.

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

### Additional Containers

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

## Grid

### How it works

The grid is pretty standard — you create rows with `.row-md` or `.row-lg` and individual columns with a `.col-*` class. Here's how it works:

- Add a `.container` to encapsulate everything and provide ample horizontal gutter space.
- Create your outer row to clear the floated columns with `<div class="row-md">` or `<div class="row-lg">`.
- Add your columns with individual `<div class="row-...">`s.

### Demo

In practice, your columns will look like the example below.

{% example html %}
<div class="container example">
  <div class="row-md">
    <div class="col-2">
      .col-2
    </div>
    <div class="col-10">
      .col-10
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

## Cards

Cards are used to display modular content. A `.card-container` is used to wrap the content and individual cards can be stacked inside of columns (within a `.card-row-md`).

{% example html %}
<div class="card-container example">
  <div class="card-row-md">
    <div class="col-4">
      <div class="card">
        .card
      </div>
    </div>
    <div class="col-4">
      <div class="card">
        .card
      </div>
    </div>
    <div class="col-4">
      <div class="card">
        .card
      </div>
    </div>
  </div>
</div>
{% endexample %}

### Sections

Sections are used to define separate areas within a single card. A lone section may be used to add padding to a card. Sections can have headings too (`.section-header`).

{% example html %}
<div class="card-container example">
  <div class="card">
    <div class="section">
      .section
    </div>
  </div>
</div>
{% endexample %}

#### Actionable Sections
To denote an interactive section add the `.actionable` class or use `a` tags instead of a `div`.

{% example html %}
<div class="card-container example">
  <div class="card">
    <div class="section actionable">
      .section .actionable
    </div>
    <a class="section">
      .section (anchor)
    </a>
  </div>
</div>
{% endexample %}

#### Padding Options
You can change the sections default padding by adding the following classes `.no-padding`, `.padding-sm`, or `.padding-lg`.

{% example html %}
<div class="card-container example">
  <div class="card">
    <div class="section no-padding">
      .section .no-padding
    </div>
    <div class="section padding-sm">
      .section .padding-sm
    </div>
    <div class="section padding-lg">
      .section .padding-lg
    </div>
  </div>
</div>
{% endexample %}

### Demo

 Putting it all together. There is also a built in class `.no-background-color` that creates a nearly transparent card. We have also built out a header that works well inside of the `.card-container`.
 
 The default background color for a card is white, but you can change this by overriding the `background-color` property in the `.card` class. 
 
 {% highlight scss %}
 .card {
   &.green-background {
     background-color: $color-green;
   }
 }
 {% endhighlight %}

{% example html %}
<div class="card-container example">
  <div class="header row-md">
    <div class="col-6">
      <div class="title">Hello World</div>
    </div>
    <div class="col-6">
      <div class="buttons">
        <button class="button secondary-action">Action</button>
      </div>
    </div>
  </div>
  <div class="card-row-md">
    <div class="col-4">
      <div class="card">
        <div class="section section-header">
          .section .section-header
        </div>
        <div class="section actionable">
          .section .actionable
        </div>
        <div class="section actionable">
          .section .actionable
        </div>
      </div>
    </div>
    <div class="col-8">
      <div class="card green-background">
        <div class="section">
          .card .green-background
        </div>
      </div>
      <div class="card no-background-color">
        <div class="section">
          .card .no-background-color
        </div>
      </div>
    </div>
  </div>
</div>
{% endexample %}
