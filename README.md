# Grid Lines

here we are going to position our element inside grid layout.    


1. first make 6*4 gird using "grid-template-columns" and "grid-template-row".   

```css
#content{
    /* ... */
    display: grid;
    grid-template-columns: repeat(6, 1fr);
    grid-template-rows: repeat(4, minmax(150px, auto));
}
```

2. set first("one") element in position in 6*4 gird layout that we created before using "grid-column-start" and "grid-row-end".  

```css
.one{
   grid-column-start:1;
   grid-column-end:3;
}
```


3. show how to combine "grid-column-start" and "grid-row-end" with "gird-column".
```css
.one{
   grid-column: 2/3;
}
```

4. show how to change elements default order using "grid-column" and "grid-row".

```css
.six{
    grid-column: 1/2;
    grid-row: 1/2;
}
```