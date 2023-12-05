# Grid Rows
why not flex box : 
1. flex box is good for only one direction. (row or column direction)
2. not care about order of the element and then we need to ezaly change order of the elements.
3. we can re-arrage the content according to screen size.  


#### Rows  

1. By adding long text to one column of the row, show row height getting content max height from one of the column.   


```html
	<div id="content">
		<div>1</div>
		<div>2</div>
		<div> add long text here ... </div>
		<div>4</div>
		<div>5</div>
		<div>6</div>
		<div>7</div>
		<div>8</div>
		<div>9</div>
	</div>
```   

2. show how to set following height to row.    

* set fixed height to row using "grid-auto-rows".    
```css
#content{
    /*... */
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-auto-rows: 200px; /* +add */
}
  
```

* set min and max height to row using "grid-auto-rows".(minmax(min height, max height))
```css
#content{
    /*... */
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-auto-rows: minmax(200px, auto); /* +add */
}
```

* set custom with each row using "gird-template-rows"    

```css
#content{
    /*... */
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: 200px 300px 400px 200px;  /* +add */
}
```

* use repeat function with "grid-template-rows" when we have many rows set same height. 

```css
#content{
    /*... */
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    /*grid-template-rows: repeat(3, 200px);*/ /* +add */
    grid-template-rows: repeat(3, minmax(200px, auto));  /* +add */
}
```

3. show how to add gap between colunm.    

here we can use margin but it goes to all around the elements but 'gap' only between elements only.    

```css
#content{
    /*... */
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(3, minmax(200px, auto));
    grid-column-gap: 10px; /* +add */
    grid-row-gap: 5px; /* +add */
    /*grid-gap:10px*/ /*combine of column and row gap*/
}
```