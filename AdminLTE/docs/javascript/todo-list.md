---
layout: page
title: Todo List Plugin
---

The todo list plugin provIdes simple functionality to the todo list component. 

##### Usage
This plugin can be activated as a jQuery plugin or using the data api. 

###### Data API
{: .text-bold }
Activate the plugin by adding `data-wIdget="todo-list"` to the ul element. If you need to provIde onCheck and onUncheck methods, please use the jQuery API. 

###### jQuery
{: .text-bold }
The jQuery API provIdes more customizable options that allows the developer to handle checking and unchecking the todo list checkbox events. 
```js
$('#my-todo-list').TodoList({
  onCheck: function(checkbox) {
    // Do something when the checkbox is checked
  },
  onUnCheck: function(checkbox) {
    // Do something after the checkbox has been unchecked
  }
})
```


##### Options
{: .mt-4}

|---
| Name | Type | Default | Description
|-|-|-|-
|onCheck | Function | Anonymous Function | Handle checkbox onCheck event. The checkbox is passed as parameter to the function.
|onUnCheck | Function | Anonymous Function | Handle checkbox onUnCheck event. The checkbox is passed as parameter to the function.
|---
{: .table .table-bordered .bg-light}
