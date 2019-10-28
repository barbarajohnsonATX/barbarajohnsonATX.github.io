---
layout: post
title:      "`this` Keyword"
date:       2019-10-28 02:38:09 +0000
permalink:  this_keyword
---


In a **constructor** function, this points to self. In the example below, an instance of Dog is created and `this` refers  to
Dog {name: "Scooby Doo"}. It is bound to the new object being constructed.

```
class Dog { constructor()
{ 
  this.name = "Scooby Doo"; 
  console.log("this", this) 
}}
 
let dog = new Dog()

> this Dog {name: "Scooby Doo"}
```


Outside of object instances, `this` takes on a new meaning. In the example below, `this` points to the object **Window**, since it was called from the **global scope**.

```
function someFunction()
{
  console.log(this) 
}
 
someFunction()
> Window {parent: Window, postMessage: ƒ, blur: ƒ, focus: ƒ, close: ƒ, …}
```

When a function is called as a **method** of an object,  `this` is set to the object the method is called on. In the example below, when shirt.f() is called inside the function, `this` is bound to the shirt object.

 
```
 var shirt = {
  type: "button down",
  f: function() {
    return this.type;
  }
};
 
console.log(shirt.f())
> button down
```

As a DOM event handler, `this` is set to the element the event fired from. In the example below, when the Edit Dog button is clicked, the editDog() handler is invoked. 


```
function addDogsClickListeners() {
     document.querySelectorAll('.dog-name').forEach(element => {
        element.addEventListener("click", showMoreInfo)
    })

    document.querySelectorAll('.edit-dog-button').forEach(element => {
        element.addEventListener("click", editDog)
    })

    document.querySelectorAll('.delete-dog-button').forEach(element => {
        element.addEventListener("click", deleteDog)
    })
    
}


```

Inside editDog(), `this` refers the button element from which the event fired. 
`<button class="edit-dog-button" style="background-color:orange">Edit Info</button>`


