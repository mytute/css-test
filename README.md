# center in parent.

here we are going to position our element inside grid layout.    


1. using flexbox.   

```css
.parent{
    /* ... */
    display: flex;
    justify-content: center;
    align-items: center;
}
```

2. using grid.   

```css
.parent{
    /* ... */
    display: grid;
    place-content:center;
}
```

3. using position.   

```css
.parent{
    /* ... */
    position:relative;
}

.child{
    /* ... */
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
}
```

4. using flexbox and margin.   

```css
.parent{
    /* ... */
    display:flex;
}

.child{
    /* ... */
    margin:auto
}
```

5. using grid and margin.   

```css
.parent{
    /* ... */
    display:grid;
}

.child{
    /* ... */
    margin:auto
}
```



