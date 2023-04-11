# Creating Classes in TypeScript

TypeScript is used to create a blueprint for creating objects (classes). It inherits the feature from ES6 class functionality. These are fundamental entities used to create reusable objects. A TypeScript classes are converted into JavaScript functions.

## Classes in TypeScript

Behave and operarate just like other languages (i.e., C#, Java) with `constructors`, `properties`, and `methods`.

## Object and Constructor

An object can be created out of a class using a "new" keyword.

```JS
var data = new Employee()
```

A **constructor** gets invoked when a class is initialized; a constructor is a function is a good place to put some logic - how the object is created.

When an object is created new memory space is created. Once the class has executed, the new memory reference is returned. The memory reference is saved to the variable `data`, in this example.

## Adding Access Modifiers to Classes

| Public                        | Private                              | Protected                         |
| ----------------------------- | ------------------------------------ | --------------------------------- |
| Any other class can access it | Cannot be accessed outside the class | private to the class and subclass |
