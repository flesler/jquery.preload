# jQuery.Preload Changelog

## 1.1.0
### Feature
- Added `srcAttribute` option so URL can be taken from other DOM attributes, thanks @emri99

## 1.0.8
### Feature
- Added `index` to the data object passed to callbacks.
- Added setting `enforceCache` to avoid images from being "un-cached"
### Optimization
- Removed some code from the preloaders(images) creation.
### Enhancement
- The image used internally for preloading is exposed in the data object as `element`.
- Removed the use of $.browser for 1.3
### Fix
- Added a (still commented) code for images that were already cached, TODO: try it

## 1.0.7
### Feature
- The onAbort event of images is checked too.

## 1.0.6
### Feature
- Patched IE's stack overflows error when preloading +15 images.
- Added a subtle change, that now allows a nifty combination of 2 modes( rollover+placeholder )
### Change
- Changed the default threshold to 2, that seems optimum.
### Fix
- Sometimes IE throws an odd error, when trying to unbind in the end.
### Optimization
- Empty urls or images/links with empty urls are now ignored.

## 1.0.5
### Change
- Relicensed from GPL to GPL+MIT.
### Fix
- Fixed the problem for Safari 2, which doesn't seem to like the "new Image()", used `$('<img />')` instead.
  Kudos to Ben Southall for helping me test and fix this.
- Even if the threshold is 0 or less, one image is used to preload.
- If no valid image is submitted, onComplete is called anyway.


## 1.0.4
### Fix
- While doing some "by-hand" optimizations for minified code, I seem to broke something for URL mode. Now it's fixed.

## 1.0.3
### Fix
- Reverted one of the optimizations as it's not compatible with jQuery +1.2.2.

## 1.0.2
### Optimization
- Slightly reduced the code size.

## 1.0.1
- Had a small bug

## 1.0.0
- First release, the plugin counts with 4 modes: URL, Link, Rollover and Placeholder.
