# intor & Grid Columns
why not flex box : 
1. flex box is good for only one direction. (row or column direction)
2. not care about order of the element and then we need to ezaly change order of the elements.
3. we can re-arrage the content according to screen size.  


#### Columns  

* we can have any count of columns and rows.  

1. create 'index.html' and add following html code for it.    

```html  
<!DOCTYPE html>
<html>
<head>
	<title>Using CSS Grid</title>
	<style>
		body{
			color: #fff;
			font-family: 'Nunito Semibold';
			text-align: center;
		}
		#content{
			max-width: 960px;
			margin: 0 auto;
		}
		#content div{
			background: #3bbced;
			padding: 30px;
		}
		#content div:nth-child(even){
			background: #777;
			padding: 30px;
		}
	</style>
</head>
<body>

	<div id="content">

		<div>1</div>
		<div>2</div>
		<div>3</div>
		<div>4</div>
		<div>5</div>
		<div>6</div>
		<div>7</div>
		<div>8</div>
		<div>9</div>

	</div>

</body>
</html>
```

2. for start convert 'content' to grid add 'display:gid' and see nothing changed.   


4. using 'grid-template-column: 33.3% 33.3% 33.3%;' for add equal size 3 column to one row.   
* row can have only 3 column because of we are define 3 with and it will repeat to other elements too.    
```css 
#content{
    max-width: 960px;
    margin: 0 auto;

    display: grid; /* +add */
    grid-template-columns: 30% 20% 50%; /* +add */
}
```

5. instead of using precentage use fraction(fr) to define "grid-template-columns".  

```css 
#content{
    max-width: 960px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr 2fr 1fr /* +add */
}
```    

6. add 'repeat()' function to repeat 1fr to 3 times. (this will helpfull when we have more column).    

```css 
#content{
    max-width: 960px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: repeat(3, 1fr);/* +add */
}
```    
