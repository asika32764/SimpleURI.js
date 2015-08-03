# SimpleURI.js

A simple JS URI object without jQuery.

## Usage

``` javascript
var uri = new URI('http://yourhost.com');

uri.path = 'some/dir';
uri.port = 8080;

uri.setQuery({flower: 'sakura', tree: 'santa'});
uri.setVar('foo', 'bar');

uri.toString();
```

### No Conflict

``` php
var SimpleURI = URI.noConflict();

// OR

var MyURI = SimpleURI.noConflict();
```
