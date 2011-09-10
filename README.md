# Backbone-browserify
## packaged for use with [node-browserify](https://github.com/substack/node-browserify).

**Important:** You must require `jquery-browserify` or Zepto (untested) with Browserify before you require Backbone, just like normal.

Just add it to your browserify require list and use it! Make sure you also have Underscore installed via npm as Backbone will automatically require it.

### Server Side
````javascript
browserify({
  require : [ 'jquery-browserify', 'backbone-browserify' ]
});
````

... or to alias it to just "backbone":

````javascript
browserify({
  require : { jQuery: 'jquery-browserify', backbone: 'backbone-browserify' }
});
````

### Client Side
````javascript
var $ = jQuery = require('jquery-browserify'),
    Backbone = require('backbone-browserify'),
    MyView = Backbone.View.extend({
        defaults: {
            title: 'Horay'
        }
    });
````

... or if you aliased it to 'backbone':

````javascript

var $ = jQuery = require('jquery'),
    Backbone = require('backbone'),
    MyView = Backbone.View.extend({
        defaults: {
            title: 'Horay'
        }
    });
````