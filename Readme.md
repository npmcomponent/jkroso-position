*This repository is a mirror of the [component](http://component.io) module [jkroso/position](http://github.com/jkroso/position). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/jkroso-position`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# position

DOM element position utilities

## Installation

_With [component](//github.com/component/component), [packin](//github.com/jkroso/packin) or [npm](//github.com/isaacs/npm)_

    $ {package mananger} install jkroso/position

then in your app:

```js
var position = require('position')
```

## API

### position()

  Get the location of the element relative to the top left of the documentElement
  
  `-> {top, right, bottom, left, width, height}` in pixels

### offset()

  Get the position of one element relative to another
  
```js
offset(child)
offset(child, parent) // => {x, y}
```

### containerBox()

  Determine the perimeter of an elements containing block. This is the box that
  determines the childs positioning. The container cords are relative to the 
  document element not the viewport; so take into account scrolling.

### offsetParent()

  Get the element that serves as the base for this ones positioning.
  If no parents are postioned it will return undefined which isn't 
  what you might expect if you know the offsetparent spec or have 
  used `jQuery.offsetParent`

## Running the tests

  Run `make`