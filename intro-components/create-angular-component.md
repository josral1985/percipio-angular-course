# Creating a Simple Angular Component

```BASH
# navigate to angular application directory
ng generate component home # creates a new component named "home".

# It creates a new folder inside `src/app/` and in it creates the home.component.ts,
# home.component.spec.ts, home.component.html, and home.component.html
# it also modifies the app.module.ts file making sure that Angular is aware of this
# new component and is ready to use (imported)
```

> command shortcut: `ng g c home`

`home.component.ts` is created with the below code:

```JS
import { Component, OnInit } from '@angular/core'

@Component({
  selector: 'app-home',
  templateUrl: './home.component.html',
  styleUrls: ['./home.component.css']
})
export class HomeComponent implements OnInt {

  constructor() {}

  ngOnInit(): void {}

}
```

`home.component.html` is created with the following default:

```HTML
<p>home works!</p>
```

To be able to see the contents of this newly created component, `app.component.html` needs to be modified by adding the new component's `selector`.

```HTML
<app-home></app-home>
```
