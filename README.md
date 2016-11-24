# SimpleURI.js

A simple JS URI object without jQuery.

## Usage

``` javascript
var uri = new URI('http://yourhost.com');

uri.path = 'some/dir';
uri.port = 8080;

uri.setQuery({flower: 'sakura', tree: 'santa'});
uri.setVar('foo', 'bar');

// get var
var foo = uri.getVar('foo');

uri.toString();
```

## Get & Set Uri Data

``` js
// Get
var scheme = uri.scheme;

// Set
uri.scheme = 'ftp';
```

## All Uri Data

``` js
var uri = new URI('https://apple:1234@example.com:8080/flower/sakura?foo=bar#orange');

uri.scheme = 'https';
uri.username = 'apple';
uri.password = '1234';
uri.host = 'example.com';
uri.port = 8080;
uri.path = 'flower/sakura';
uri.query = {foo: 'bar'};
uri.hash = 'orange';
```

## Build query

``` js
uri.httpBuildQuery({a: 'b', c: 'd'}); // a=b&c=d

// separator as second argument
uri.httpBuildQuery({a: 'b', c: 'd'}, '&amp;'); // a=b&amp;c=d
```

### No Conflict

``` php
var SimpleURI = URI.noConflict();

// OR

var MyURI = SimpleURI.noConflict();
```
