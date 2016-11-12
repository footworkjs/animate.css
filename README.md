# footwork-animate

*Just-add-water CSS animation (for FootworkJS)*

Custom/forked version of [animate.css](https://github.com/daneden/animate.css) for usage with [FootworkJS](https://github.com/footworkjs/footwork) when animating its elements.

**NOTE:** This version of [animate.css](https://github.com/daneden/animate.css) has been modified to be [SASS](http://sass-lang.com/)-based and to use a flag on the parent element to trigger the changed state/animation on its direct children.

## Installation

To install via Bower, simply do the following:

```bash
$ bower install footwork-animate --save
```
or you can install via npm:

```bash
$ npm install footwork-animate --save
```

## Basic Usage

1. Include the stylesheet on your document's `<head>`

  ```html
  <head>
    <link rel="stylesheet" href="/bower_components/footwork-animate/animate.min.css">
  </head>
  ```

2. Add the class `animatedIn` to the parent element of the element you want to animate into view.

3. Finally you need to add one of the following classes to the elements (direct children of the parent) you want to animate:

  * `fadeIn`
  * `fadeInDown`
  * `fadeInDownBig`
  * `fadeInLeft`
  * `fadeInLeftBig`
  * `fadeInRight`
  * `fadeInRightBig`
  * `fadeInUp`
  * `fadeInUpBig`
  * `flipInX`
  * `flipInY`
  * `lightSpeedIn`
  * `rotateIn`
  * `rotateInDownLeft`
  * `rotateInDownRight`
  * `rotateInUpLeft`
  * `rotateInUpRight`
  * `rollIn`
  * `zoomIn`
  * `zoomInDown`
  * `zoomInLeft`
  * `zoomInRight`
  * `zoomInUp`
  * `slideInDown`
  * `slideInLeft`
  * `slideInRight`
  * `slideInUp`

Full example:
```html
<div class="contents">
  <!-- Any element with one of the above animations is invisible until
       its parent has the animatedIn class added. -->
  <h1 class="fadeInUp">Example fadeInUp</h1>
  <h1 class="flipInX">Example flipInX</h1>
</div>
```

```javascript
/**
 * All of the direct children of the parent will then have their
 * animations triggered when the animatedIn class is added to the parent.
 */
$('.contents').addClass('animatedIn');

// removing the animatedIn class will cause the element to reset to original starting, invisible state
$('.contents').removeClass('animatedIn');
```

## Custom Builds
footwork-animate is powered by [gulp.js](http://gulpjs.com/), and you can create custom builds pretty easily. First of all, you’ll need Gulp and all other dependencies:

```sh
$ cd path/to/footwork-animate/
$ sudo npm install
```

Next, run `gulp` to compile your custom builds. For example, if you want only some of the “fading entrances”, simply edit the `animate-config.json` file to select only the animations you want to use.

```javascript
"fading_entrances": {
  "fadeIn": true,
  "fadeInDown": false,
  "fadeInLeft": true,
  "fadeInLeftBig": true,
  "fadeInRight": false,
  "fadeInRightBig": true,
  "fadeInUp": false,
  "fadeInUpBig": true
}
```

## License
footwork-animate is licensed under the MIT license. (http://opensource.org/licenses/MIT)
