# Grid Areas

here we are define element position using "grid-template-areas".    


1. add following html tag to html file.    

```html
<div id="content">

    <header>Header</header>
    <main>Main</main>
    <section>Section</section>
    <aside>Aside</aside>
    <nav>Nav</nav>
    <footer>Footer</footer>
    
</div>
```    

2. add following css to convert above html to grid.  

```css 
#content{
    max-width: 960px;
    margin: 0 auto;

    display: grid; /* add here */ 
    grid-template-columns: repeat(4,1fr); /* add here */ 
    grid-auto-rows: minmax(100px, auto); /* add here */ 
}
```

3. show how to assign "grid-area" property with it's unique name.    
```css 
header{
    grid-area: header;
}
main{
    grid-area: main;
}
aside{
    grid-area: aside;
}
nav{
    grid-area: nav;
}
section{
    grid-area: section;
}
footer{
    grid-area: myGridArea;
}
```


4. then show how to add "grid-template-areas" property with each line as a row with assign name of "grid-area".   

here you can use "." symbol to add blank element.   

```css
#content{
    /* ... */
    grid-gap:10px;
    grid-template-areas: 
    "header header header header"
    "aside . main main"
    "nav nav main main"
    "section section section section"
    "myGridArea myGridArea myGridArea myGridArea"
}
```