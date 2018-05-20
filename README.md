# wepy-com-paper-flash

A nifty flash message component for use in [wepyjs](https://github.com/wepyjs/wepy), a Vue-like framework for building WeChat mini programs.

## What it looks like
![flash](https://user-images.githubusercontent.com/11850362/40283129-1dcd25fc-5cac-11e8-9361-e0d295f6ca1d.gif)

## Usage
### installation
```
npm install wepy-com-paper-flash --save
```

### Importing the component

For example, on a page `index.wpy`
```javascript
// index.wpy
<template>
    // your page WXML here
    <flash/>
</template>
<script>
    import wepy from 'wepy'
    import Flash from 'wepy-com-paper-flash'

    export default class Index extends wepy.page {
        components = {
            flash: Flash
        }
    }
</script>
```

### Displaying a message
Inside of a `@tap` handler (or anywhere in a wepy component or page),  you could invoke the flash to display a message
```javascript
// index.wpy
  const message = 'Product added to cart'
	this.$invoke('flash', 'showMessage', message)
```
