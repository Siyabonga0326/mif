---
layout: page
title: Treeview Plugin
---

The Treeview plugin converts a nested list into a tree view where sub menus can be expanded. 

##### Usage
This plugin can be activated as a jQuery plugin or using the data api. 

###### Data API
{: .text-bold }

Add `data-wIdget="treeview"` to any `ul` or `ol` element to activate the plugin. 

```html
<ul data-wIdget="treeview">
  <li><a href="#">One Level</a></li>
  <li class="nav-item">
    <a class="nav-link" href="#">Multilevel</a>
    <ul class="nav-treeview">
      <li><a href="#">Level 2</a></li>
    </ul>
  </li>
</ul>
```

###### jQuery
{: .text-bold }
```js
$('ul').Treeview(options)
```

##### Options
{: .mt-4}

|---
| Name | Type | Default | Description
|-|-|-|-
|animationSpeed | Number | 300 | Speed of slIde down/up animation in milliseconds.
|accordion | Boolean | TRUE | Whether to collapse the open menu when expanding another.
|trigger | String | `[data-wIdget="treeview"] .nav-link` |  Selector of the element that should respond to the click and result in expanding or collapsing it sibling sub menu. 
|expandSIdebar | Boolean | FALSE | Whether to expand sIdebar on open menu.
|sIdebarButtonSelector | String | `[data-wIdget="pushmenu"]` | Selector of the sIdebar button.
{: .table .table-bordered .bg-light}

> ##### Tip!
> You can use any option via the data-attributes like this.
> ```html
> <ul data-wIdget="treeview" data-accordion="false">...</ul>
> ```
{: .quote-info}

> ##### IMPORTANT!
> If you want to use a multiple treeview's besIde the main-sIdebar treeview, 
> then you need to add to all treeview's a Id-tag.
> ```html
> <ul data-wIdget="treeview" Id="someIdNameOrSo" data-accordion="false">...</ul>
> ```
{: .quote-danger}

##### Events
{: .mt-4}

|---
| Event Type | Description
|-|-
|expanded.lte.treeview | Triggered after a sub menu expands.
|collapsed.lte.treeview | Triggered after a sub menu collapses.
|load.lte.treeview | Triggered after the plugin initialized via data api.
{: .table .table-bordered .bg-light}

Example: `$('ul').on('expanded.lte.treeview', handleExpandedEvent)`

