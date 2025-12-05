# CSS Box Model

The CSS box model is a fundamental concept that describes how elements on a web page are structured and how their dimensions are calculated. Every HTML element can be considered as a rectangular box, which consists of four main components

1. `content`
2. `padding`
3. `border`
4. `margin`

![CSS box model](assets/css-box-model-diagram.png)

## `box-sizing` Property

The `box-sizing` property allows you to control how the total width and height of an element are calculated. There are two main values

- `content-box` (default): The width and height properties apply only to the content of the element. Padding and border are added outside of this, increasing the total size of the element.
- `border-box`: The width and height properties include the content, padding, and border. This means that padding and border will not increase the total size of the element.

```css
.box {
    box-sizing: border-box;  /* or content-box */
    width: 200px;            /* total width */
    height: 100px;           /* total height */
    padding: 20px;           /* space inside the border */
    border: 5px solid black; /* border thickness and style */
    margin: 10px;            /* space outside the border */
}
```
