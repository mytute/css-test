# Grid Areas

Here we see how to add media query with grid.    

1. show how to add media with query. 

This is normal way to add media query for css 

```css
    #content{
        max-width: 960px;
        margin: 0 auto;
        display: grid;
        grid-template-columns: repeat(4,1fr);
        grid-auto-rows: minmax(100px, auto);
        grid-gap:10px;
        grid-template-areas: 
        "header header header header"
        "aside . main main"
        "nav nav main main"
        "section section section section"
        "myGridArea myGridArea myGridArea myGridArea"
    }
    @media screen and (max-width: 760px){
        #content{
            max-width: 960px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(4,1fr);
            grid-auto-rows: minmax(100px, auto);
            grid-gap:10px;
            grid-template-areas: 
            "header header header header"
            "aside aside main main"
            "nav nav main main"
            "section section section section"
            "myGridArea myGridArea myGridArea myGridArea"
        }
    }
```
