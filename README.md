# Animate

`animate.js` is a tiny library that helps you write smooth CSS-powered animations in JavaScript. See
a quick demo of 500 elements animating at
[playground.deaxon.com/js/animate](http://playground.deaxon.com/js/animate/).

# Usage

Include `animate.min.js` in your page:
```html
<script src=animate.min.js></script>
```

Start animating things:
```javascript
animate({
  el: "div",
  translateX: 100,
  opacity: .5,
  duration: 500,
  complete: function() { alert("Done!") }
});
```

# API

`animate` requires a config object accepting the following options:

## el
The elements you want to animate. `el` can be a:

* CSS selector
* DOM element
* array of DOM elements
* NodeList or HTMLCollection

## duration
[Optional] The duration of your animation in milliseconds. Default: 400. `ms` will be added if you don't specify a
unit.

## delay
[Optional] The delay before your animation starts in milliseconds. Default: 0. `ms` will be added if you don't specify a
unit.

## easing
[Optional] The animation curve (CSS keyword or cubic-bezier). Default: ease.

## complete
[Optional] A function called at the end of the animation. Inside the function, `this` refers to the
DOM element that has finished animating.

## animatable properties
* opacity
* translateX
* translateY
* translateZ
* scaleX
* scaleY
* scaleZ
* rotateX
* rotateY
* rotateZ
* skewX
* skewY
* perspective

You can also use the shortcut transform functions `translate`, `scale` and `rotate` when the same
value should be applied to X and Y:

```javascript
translate: 100 // same as translateX: 100, translateY: 100
```

If you don't specify a unit, `px` will be added to `translate`-related and `perspective` functions and `deg`
to `rotate`-related functions.
