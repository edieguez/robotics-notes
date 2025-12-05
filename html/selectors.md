# CSS Selectors

## Attribute selectors

```css
/* Links with "wiki" anywhere in the URL */
a[href*="wiki"] {
  color: green;
}

/* Links with URL that starts with "#" */
a[href^="#"] {
  color: blue;
}

/* Links with URL that ends with "org" */
a[href$="org"] {
  color: orange;
}
```

## Selector list

```css
/* Style all <h1> and <p> elements */
h1, p {
  margin-bottom: 20px;
}
```

## Descendant combinator

```css
/* Style all <em> elements inside <p> elements */
p em {
  font-style: normal;
  color: red;
}
```

## Child combinator

```css
/* Style only direct <li> children of <ul> */
ul > li {
  list-style-type: square;
}
```

## Adjacent sibling combinator

```css
/* Style the <p> that immediately follows an <h2> */
h2 + p {
  font-weight: bold;
}
```

## General sibling combinator

```css
/* Style all <p> elements that are siblings of an <h2> */
h2 ~ p {
  color: gray;
}
```
