# Working with exports/import Array

If we want to an external JavaScript file we can do it on the `src/assets` directory (creating a new subdirectory named `JS` for demo). Once the file is created we have to let the application know.

```JS
// src/assests/JS/randomgen.js
genRandomNumbers = () =>{
  let rNum = [];

  for (let i = 0; i < 10; i++){
    let rnd = Math.floor((Math.random() * 9999) + 1);
    rNum.push(rnd);
  }

  return rNum;
}
```

To let the Angular know about this new file we must edit the `angular.json` config file (found in the root directory of application).

```JS
// angular.json
{
  ...,
  "projects": {
    "skills": {
      ...,
      "achitect": {
        "build": {
          ...,
          "options": {
            ...,
            "scripts": [
              "src/assets/JS/randomgen.js"
            ]
            ...
```

Now we can use the JavaScript code! We declare the function in the desired component and then inside the class itself we can use it.

```JS
//product-components.ts
import { Component } from '@angular/core';

//declaring function
declare const genRandomNumbers: any;

@Component({
  selector: 'app-product',
  templateUrl: './product.component.html',
  styles: ['div {font-weight: bolder; color:darkgreen;}'],
})
export class ProductComponent {
  showDiv = true;

  rNum = <[]>genRandomNumbers(); // pointing to the function inside the javascript expecting
  // an array (using generics)

  // this should display an array of 10 random numbers
  // use the template for display using string intrepolation
}
```

```HTML
<!-- product.component.html -->
<h2>Product Files</h2>
<div *ngIf="showDiv">Product 1</div>
<div>{{rNum}}</div>
```

![Output](img/output.png)
