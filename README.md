# footwork-animate

[![npm version](https://badge.fury.io/js/footwork-animate.png)](https://badge.fury.io/js/footwork-animate) [![Bower version](https://badge.fury.io/bo/footwork-animate.png)](https://badge.fury.io/bo/footwork-animate)

*Just-add-water CSS animation (for FootworkJS)*

This is a CSS library/toolset used to animate elements into and out of view. Elements are animated into and out of the browser by using a parent flag which triggers a CSS animation on its nested children.

* **NOTE**: This library can be used independently, but was developed for usage with [FootworkJS](https://github.com/footworkjs/footwork) when animating its elements.
* **NOTE**: Based on/heavily customized version of [animate.css](https://github.com/daneden/animate.css).

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

1. You need to add one of the following classes to the elements (direct children of the parent) you want to animate:

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

1. Finally, add the class `animateIn` to the parent element of the elements you want to animate into view.

  Full example:

  ```html
  <div class="contents">
    <!-- Any element with one of the above animations is invisible until
        its parent has the animateIn class added. -->
    <h1 class="fadeInUp">Example fadeInUp</h1>
    <h1 class="flipInX">Example flipInX</h1>
  </div>
  ```

  ```javascript
  /**
  * All of the direct children of the parent will then have their
  * animations triggered when the animateIn class is added to the parent.
  */
  $('.contents').addClass('animateIn');

  // removing the animateIn class will cause the element to reset to original starting, invisible state
  $('.contents').removeClass('animateIn');
  ```

## Custom Builds

footwork-animate is offered in both SCSS and plain (compiled) CSS form. You can either include the supplied SCSS and customize your build that way or you can clone the repo, modify the source, and rebuild as described below:

1. Clone the repo from GitHub:

  ```sh
  git clone https://github.com/footworkjs/footwork-animate.git
  cd footwork-animate
  ```

1. Install Node.js and NPM (if needed):

  This is platform specific. Your OS may already include it, however if not please see: [Installing Node](https://docs.npmjs.com/getting-started/installing-node).

1. Install [gulp](http://gulpjs.com/) globally (if needed):

  ```sh
  sudo npm install -g gulp-cli
  ```

1. Next, run `gulp` from the footwork-animate folder to compile your custom builds.

  ```sh
  gulp
  ```

  If you want only some of the “fading entrances”, simply edit the `animate-config.json` file to select only the animations you want to use.

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

## Available SASS Variables/Defaults

If you are making your own custom build using the SCSS, you have these available variables you can override:

```SASS
// The class added to the parent which triggers the animation on its children
$animateInClass: 'animateIn';

// The duration of the animations
$animateInDuration: 0.6s;

// For animations that 'slide' elements, this is the 'normal' distance
$normalDistance: 100px;

// For animations that 'slide' elements, this is the 'big' distance
$bigDistance: 200px;

@import "/path/to/footwork-animate/animate.scss";
```

## License
footwork-animate is licensed under the MIT license. (http://opensource.org/licenses/MIT)
