# Aligning and Justifying Items

here we see how to aling item inside element when it is in grid container.   

If the grid box is the same size as the content, then no changes will be apparent after applying the following properties, especially in terms of height. 

1. show how to align items for all items inside container by using "align-items" and "justify-items".      

```css 
#content{
    max-width: 960px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap:10px;

    align-items: end; /* start,end, default: stretch */
    justify-items: left; /* start,end, default: stretch */

}
```

1. show how to align items by single(individual) element by using "align-self" and "justify-self".  

```css
.one{
    align-self: start; /* start,end,center default: stretch */
    justify-self: center; /* start,end,center default: stretch */
}
```