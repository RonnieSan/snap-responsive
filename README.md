# snap-responsive
A simple repo for adding snap responsiveness to a website

## Installation
```bash
npm install snap-responsive
```
## Usage
Import and call the init method. You can pass in optional snap sizes or use the defaults.
```js
import { SnapResponsive } from 'snap-responsive';

window.onload = function() {
  SnapResponsive.init();
}
```

Or use custom snap sizes
```js
// Custom snap sizes
// Order is important. Put larger sizes first since it iterates through all objects
// and stops when the screen width is no longer smaller than the threshold.
const snap_sizes = [
  // Large Screens (UHD)
  {
    threshold : Infinity,
    width     : 'device-width'
  },

  // Desktop Screens (HD)
  {
    threshold : 1920,
    width: 1680
  },

  // Smaller Desktop Screens (1280x800)
  {
    threshold : 1680,
    width     : 1280
  },

  // Tablet Screens (800x600)
  {
    threshold : 1280,
    width     : 768
  },

  // Mobile Screens
  {
    threshold : 768,
    width     : 360
  }
]

// Then call init and pass in your sizes
SnapResponsive.init(snap_sizes);
```
