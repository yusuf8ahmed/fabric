---
layout: page
title: Tables
---

By default, no styles are added to the `<table>` elements. See below to see how you can add styles and responsive functionality to tables.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}


## Styles

The available classes add padding and text alignment, as follows:

- the class `.table__th` sets `text-align: left;` to the table headings `<th>`
- the classes `.table__td` and `.table__th` add padding
- the modifier class `.table--full` will set the table width to 100%

{% example html %}
<table class="table table--full">
  <thead>
    <tr>
      <th class="table__th">Name</th>
      <th class="table__th">Email</th>
      <th class="table__th">Age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td class="table__td">Carrie Lee</td>
      <td class="table__td">carrie@example.com</td>
      <td class="table__td">20</td>
    </tr>
    <tr>
      <td class="table__td">Mario García</td>
      <td class="table__td">mario@example.com</td>
      <td class="table__td">30</td>
    </tr>
    <tr>
      <td class="table__td">Madeleine Poulin</td>
      <td class="table__td">maddy@example.com</td>
      <td class="table__td">40</td>
    </tr>
    <tr>
      <td class="table__td">Patrick Fitzpatrick</td>
      <td class="table__td">pat@example.com</td>
      <td class="table__td">50</td>
    </tr>
  </tbody>
</table>
{% endexample %}


## Responsive tables

TODO
