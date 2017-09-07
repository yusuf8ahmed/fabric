---
layout: page
title: Forms
---

Style individual form controls and utilize common layouts.

<div class="flash">
  <strong>Heads up!</strong> Forms need some reworking to clean up the specificity and required markup. We'll get to that soon!
</div>

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Example form

Form elements in Fabric currently have no basic layout specified (this is by design). You'll need to use `<fieldset>`s, `<div>`s, or other elements and styles to rearrange them.

{% example html %}
<form>
  <input type="text" class="form-input-text" placeholder="Name">
  <input type="email" class="form-input-text" placeholder="Email address">
  <input type="number" class="form-input-text" placeholder="Age">

  <p>
    <label>
      <input type="checkbox"> Remember me
    </label>
  </p>

  <p>
    <label>
      <input type="radio" id="herp" name="herpderp" checked> Herp
    </label>
    <label>
      <input type="radio" id="derp" name="herpderp"> Derp
    </label>
  </p>

  <p>
    <button class="button primary-action" type="submit">Submit</button>
  </p>
</form>
{% endexample %}

## Colors

The default text inputs has a white background, but you can append the `.color-beige` class to make it beige.

{% example html %}
<form>
  <input class="form-input-text" type="text" placeholder=".form-input-text (default)">
  <input class="form-input-text color-beige" type="text" placeholder=".form-input-text .color-beige">
</form>
{% endexample %}

## Sizes

There are two input sizes: medium and small. (TODO: consider adding more sizes as necessary).

Medium is the default size, but you can apply the `.size-sm` class to make it small.

{% example html %}
<form>
  <input class="form-input-text" type="text" placeholder="medium (default)">
  <input class="form-input-text size-sm" type="text" placeholder=".size-sm">
</form>
{% endexample %}

## Selects

{% example html %}
<form>
  <select class="form-control">
    <option disabled selected default>Select a prefecture</option>
    <option>Gifu</option>
    <option>Kyoto</option>
    <option>Tokyo</option>
  </select>
  <select class="form-control size-sm">
    <option disabled selected default>Select a language</option>
    <option>JavaScript</option>
    <option>CoffeeScript</option>
    <option>TypeScript</option>
  </select>
</form>
{% endexample %}

## Checkboxes and Radios

TODO - use iCheck plugin

## Form Groups

### Input Groups

{% example html %}
<form>
  <div class="input-group">
    <input class="form-input-text size-sm" type="text" placeholder="Input">
    <button class="button primary-action">Button</button>
  </div>
</form>
{% endexample %}

### Adjacent Inputs

{% example html %}
<div class="adjacent-inputs-md">
  <input placeholder="First name"
         class="form-input-text"
         type="text">
  </input>
  <input placeholder="Last name"
         class="form-input-text"
         type="text">
  </input>
</div>
{% endexample %}

### Inline Labels

{% example html %}
<div class="form-inline">
  <div class="row-md">
    <label class="col-2 control-label">
      Label
    </label>
    <div class="col-10">
      <input placeholder="Input (default)"
             class="form-input-text"
             type="text">
      </input>
    </div>
  </div>
</div>

<div class="form-inline size-sm">
  <div class="row-md">
    <label class="col-2 control-label">
      Label
    </label>
    <div class="col-10">
      <input placeholder="Input (.size-sm)"
             class="form-input-text size-sm"
             type="text">
      </input>
    </div>
  </div>
</div>
{% endexample %}

## Form Validation

We have provided simple error styles for form elements and help messages.  The intent is that your application logic will add the `.has-error` class to form elements if there are validation errors as well as hide/show the `.help-block` when appropriate.

{% example html %}
<form>
  <div class="has-error">
    <input class="form-input-text" type="text" placeholder="Something went wrong">
    <div class="help-block">Your error message here.</div>
  </div>
</form>
{% endexample %}
