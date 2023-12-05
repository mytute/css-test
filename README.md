# Nested Grids

here we see how to nest grid in another.    

1. change 4th div's class to "nested" and inside it add 4 "p" tags. And show how to make 2*2 grid inside 4th div.  add padding, border and remove default margin of p tag for better watch the result.   

```css
.nested {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap:10px
}
.nested p {
    border: 1px solid #fff;
    padding: 20px;
    margin: 0;
}
```
2. show how to expand to full with of grid for "nested" element by using "span" keyword.     

when we using span tag because of it's start from 1, we can use 3 instead of 4 to get same result.
```css 
.nested {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap:10px;
    grid-column: span 3; /*grid-column: 1/4;*/
}
```