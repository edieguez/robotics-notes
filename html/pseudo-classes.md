# [CSS Pseudo-Classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Selectors/Pseudo-classes)

Pseudo-classes are used to define the special state of an element. They are typically used to style an element when a user mouses over it, clicks on it, or when it receives focus.

## Common Pseudo-Classes

- `:hover` - Applies when the user hovers over an element.
- `:focus` - Applies when an element has focus (e.g., an input field).
- `:active` - Applies when an element is being activated (e.g., a button being clicked).
- `:nth-child(n)` - Applies styles to the nth child of a parent element.
- `:first-child` - Applies styles to the first child of a parent element.
- `:last-child` - Applies styles to the last child of a parent element.

## Examples

```css
a:hover {
  color: red;
}

input:focus {
  border: 2px solid blue;
}

li:nth-child(2) {
  background-color: yellow;
}
```
