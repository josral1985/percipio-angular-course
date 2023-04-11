# Adding Properties to TypeScript Classes

Properties can be added to classes like other OOP languages; they store the values of those classes. Access modifiers can be added to the TypeScript properties (same public, some private, etc...) Access modifiers control the visibility of the data members, this concept is called **encapsulation**.

## Example of TypeScript Properties

```JS
class Animal {
  furColor: 'brown'; //property named furColor with value 'brown'

  //constructor
  constructor() {}

  //function
  myColor() {
    return "Hello, I am " + this.furColor;
  }
}
```
