# Adding styleUrls to Angular Components

One the component is created, the style temple (css file) is created. This template is empty.

`home.component.ts`:

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

`home.component.css`:

```CSS
div#demo {
  color: blue;
}
```

output:

![CSS](img/css-files.png)
