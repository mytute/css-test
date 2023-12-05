# Create a 12-Column Grid

Here we create custom 12 grid system with simple layout.   

1. add following tags for the "content" in html page. and add following css code to create 12*n grid system.      

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

```css
#content{
    max-width: 960px;
    margin: 0 auto;

    display: grid;
    grid-template-columns: repeat(12, 1fr); /* set column count */
    grid-auto-rows: minmax(100px, auto); /* set row min max height */
    grid-gap:10px;

}
#content >*{
    background: #3bbced;
    padding: 30px;
}
```  

2. now make positioning elements using "grid-column" and "grid-row".   

```css
    header{
        grid-column: 1 / 13;
    }
    main{
        grid-column: 4 / 13;
        grid-row: 2 / 4;
    }
    aside{
        grid-column: 1 / 4;
    }
    nav{
        grid-column: 1 / 4;
    }
    section{
        grid-column: 1 / 13;
        grid-row: 4 / 6;
    }
    footer{
        grid-column: 1 / 13;
    }
```

3. to watch grid system on the screen add following html and css.    

```html  
    <input type="checkbox" /> <!-- add here -->
	<div id="content">
        <!-- add from -->
        <div id="grid">
            <p></p><p></p><p></p><p></p><p></p><p></p><p></p><p></p><p></p><p></p><p></p><p></p>
        </div>
        <!-- add end -->
		<header>Header</header>
        <main>Main</main>
        <section>Section</section>
        <aside>Aside</aside>
        <nav>Nav</nav>
        <footer>Footer</footer>
	</div>
```   

```css

    #content{
        /* ...  */
        position:relative; /* add here */
    }
    #grid{
        position: absolute;
        top: 0;
        left: 0;
        display: grid;
        grid-template-columns: repeat(12, 1fr);
        grid-auto-rows: minmax(100%, auto);
        width: 100%;
        height: 100%;
        background: transparent;
        padding: 0;
        display: none;
    }
    input:checked + #content #grid{
        display: grid;
    }
    #grid p{
        border: 1px solid;
        background: #000;
        margin: 0;
        opacity: 0.2;
    }
```