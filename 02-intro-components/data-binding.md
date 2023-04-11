# Data Binding in Angular

The process of connecting/synchronizing data with UI elements. Helps the user to manipulate the elements on the website and defines the interaction between the DOM and the components. It allows one-way and two-way binding.

## Property Binding

Property binding binds a property of a DOM element to the class variable

**Regular HTML:** here the right side of `src` is interpreted by the browser as a location

```HTML
<img src="imageUrl.jpg" alt="">
```

**Angular property binding:** the right side is interpreted by a property in the component.

```HTML
<img [src]="image">
```

## Event Binding

It binds to the element's events to a desired function on the `component.ts` file; for example the `click` event

`home.component.ts`:

```JS
onClickEvent() {
  alert("You just clicked me!")
}
```

`home.component.html`:

```HTML
<button type="" (click)="onClickEvent()">click me</button>
```

`output`:

![Event Binding](img/event-binding.png)

## Data Binding with Interpolation

Data can be bound to the component using interpolation. Returns HTML output from TypeScript code.

`home.component.ts`:

```JS
name: string = "Jose";
```

`home.component.html`:

```HTML
<h3>Hello !!! {{ name }}!!!</h3>
```

`output`:

![Interpolation](img/string-interpolation.png)
