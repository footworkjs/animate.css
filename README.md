#Animate.css [![GitHub release](https://img.shields.io/github/release/daneden/animate.css.svg)](https://github.com/daneden/animate.css/releases) [![Build Status](https://travis-ci.org/WarenGonzaga/animate.css.svg?branch=master)](https://travis-ci.org/WarenGonzaga/animate.css) [![devDependencies Status](https://david-dm.org/WarenGonzaga/animate.css/dev-status.svg)](https://david-dm.org/WarenGonzaga/animate.css?type=dev) [![chat](https://img.shields.io/badge/chat-gitter-green.svg)](https://gitter.im/animate-css/Lobby)
*Just-add-water CSS animation*

Custom version of [animate.css](https://github.com/daneden/animate.css) for usage with [FootworkJS](https://github.com/footworkjs/footwork) when animating its elements.

**NOTE:** This version of [animate.css](https://github.com/daneden/animate.css) has been modified to be [SASS](http://sass-lang.com/)-based and to use a flag on the parent element to trigger the changed state/animation on its direct children.

## Installation

To install via Bower, simply do the following:

```bash
$ bower install animate.css --save
```
or you can install via npm:

```bash
$ npm install animate.css --save
```

##Basic Usage
1. Include the stylesheet on your document's `<head>`

  ```html
  <head>
    <link rel="stylesheet" href="animate.min.css">
  </head>
  ```
  or use the version hosted by [CDNJS](https://cdnjs.com/libraries/animate.css)
  ```html
  <head>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.5.2/animate.min.css">
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
  <h1 class="fadeInUp">Example</h1>
</div>
```

```javascript
$('.contents').addClass('animatedIn');
```

## Custom Builds
Animate.css is powered by [gulp.js](http://gulpjs.com/), and you can create custom builds pretty easily. First of all, you’ll need Gulp and all other dependencies:

```sh
$ cd path/to/animate.css/
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
Animate.css is licensed under the MIT license. (http://opensource.org/licenses/MIT)
