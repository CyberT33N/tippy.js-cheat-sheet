# tippy.js-cheat-sheet
Tippy.js Cheat Sheet


<br><br>

## Create tippy
```html
<html>
  <head>
    <title>Tippy</title>
  </head>
  <body>
    <button id="myButton">My button</button>

    <script src="https://unpkg.com/@popperjs/core@2"></script>
    <script src="https://unpkg.com/tippy.js@6"></script>
    <script>
      // With the above scripts loaded, you can call `tippy()` with a CSS
      // selector and a `content` prop:
      tippy('#myButton', {
        content: 'My tooltip!',
      });
    </script>
  </body>
</html>
```





<br><br><br><br>

## Show tooltip programmatically
```javascript
// Method #1 - Tooltip still active via hover 
const tip = tippy('.finder', {
    content: 'My tooltip!',
    showOnCreate: true
})
```


<br><br><br><br>

## Hide tooltip programmatically
```javascript
// Method #1 - I do not know why but with Tippy 6 the variable assignment of tippy() gets into an array. So we must use tip[0]
  const tip = tippy('.finder', {
    content: 'My tooltip!',
    showOnCreate: true
  })

  setTimeout(() => {
    tip[0].disable()
  }, 2000)
```
