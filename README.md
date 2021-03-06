# tippy.js-cheat-sheet
Tippy.js Cheat Sheet


<br><br>

## Create tippy
```html
<html>
  <head>
    <title>Tippy</title>
    
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/dist/backdrop.css" />
    
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/themes/light.css" />
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/themes/light-border.css" />
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/themes/material.css" />
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/themes/translucent.css" />
    
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/animations/shift-away.css" />
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/animations/scale.css" />
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/animations/perspective.css" />
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/animations/shift-toward.css" />
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
  content: 'My tooltip!'
})

setTimeout(() => {  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/dist/backdrop.css" />
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/themes/light.css" />
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/themes/light-border.css" />
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/themes/material.css" />
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/themes/translucent.css" />
  // - I do not know why but with Tippy 6 the variable assignment of tippy() gets into an array. So we must use tip[0]
  tip[0].show()
}, 2000)




// Method #2 - Tooltip still active via hover 
const tip = tippy('.finder', {
    content: 'My tooltip!',
    showOnCreate: true
})
```


<br><br><br><br>

## Hide tooltip programmatically
```javascript
// Method #1
  const tip = tippy('.finder', {
    content: 'My tooltip!',
    showOnCreate: true
  })

  setTimeout(() => {
  // - I do not know why but with Tippy 6 the variable assignment of tippy() gets into an array. So we must use tip[0]
    tip[0].disable()
  }, 2000)
```




<br><br><br><br>

## available trigger

```javascript
{
  // default
  trigger: 'mouseenter focus',
  
  // others:
  trigger: 'click',
  trigger: 'focusin',
  trigger: 'mouseenter click',
  
  // only programmatically trigger it
  trigger: 'manual',
}
```


<br><br>

### Hide tooltip only via click - trigger click
```javascript
const tip = tippy('.finder', {
  content: 'My tooltip!',
  theme: 'light-border',
  animation: 'scale',
  duration: 1000,
  trigger: 'click'
})
```



<br><br>

### Change tooltip position
```javascript
const tip = tippy(querySelector, {
    content: e,
    theme: 'light-border',
    animation: 'scale',
    trigger: 'manual',
    placement: 'bottom'
})
```












































<br><br>
____________________________________________________
____________________________________________________
<br><br>


# CSS

## Extend CSS of Theme
```js
const tip = tippy('.finder', {
  content: 'My tooltip!',
  theme: 'light-border'
})
```

```css
.tippy-box[data-theme~=light-border] {
  box-shadow: 0em 0em 25em 1.1em rgb(252 43 120 / 36%), 0.2em 0.2em 0.4em 0.1em rgb(0 0 0 / 40%)
}
```











































<br><br>
____________________________________________________
____________________________________________________
<br><br>


# Themes

## Enable
```html
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/dist/backdrop.css" />
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/themes/light.css" />
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/themes/light-border.css" />
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/themes/material.css" />
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/themes/translucent.css" />
```


<br><br>

## Usage
```javascript
  const tip = tippy('.finder', {
    content: 'My tooltip!',
    theme: 'light'
  })
```

<br><br>






































<br><br>
____________________________________________________
____________________________________________________
<br><br>


# Plugins

## followCursor
```javascript
const tip = tippy('.finder', {
  content: 'My tooltip!',
  followCursor: true
})
```

<br><br>

## animateFill (Animate Fade-in & Fade-out)
```html
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/dist/backdrop.css" />
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/animations/shift-away.css" />
```

```javascript
const tip = tippy('.finder', {
  content: 'My tooltip!',
  theme: 'light-border',
  animateFill: true
})
```


















<br><br>
____________________________________________________
____________________________________________________
<br><br>


# Animate
- Options are: shift-away, scale, perspective, shift-towards

## followCursor
```html
<link rel="stylesheet" href="https://unpkg.com/tippy.js@6/animations/shift-away.css" />
<link rel="stylesheet" href="https://unpkg.com/tippy.js@6/animations/scale.css" />
<link rel="stylesheet" href="https://unpkg.com/tippy.js@6/animations/perspective.css" />
<link rel="stylesheet" href="https://unpkg.com/tippy.js@6/animations/shift-toward.css" />
```

```javascript
const tip = tippy('.finder', {
  content: 'My tooltip!',
  animation: 'scale'
})
```











  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/animations/shift-away.css" />
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/animations/scale.css" />
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/animations/perspective.css" />
  <link rel="stylesheet" href="https://unpkg.com/tippy.js@6/animations/shift-toward.css" />

