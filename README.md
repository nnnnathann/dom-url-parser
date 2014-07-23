URL Parsing for the Browser
============

Parse URL using snippet from here: http://james.padolsey.com/javascript/parsing-urls-with-the-dom/

USAGE
=====

#### As Global

```html
<script src="bower_components/dom-url-parser.js"></script>
<script>
  var myURL = domUrl('http://abc.com:8080/dir/index.html?id=255&m=hello#top');
  myURL.file;     // = 'index.html'
  myURL.hash;     // = 'top'
  myURL.host;     // = 'abc.com'
  myURL.query;    // = '?id=255&m=hello'
  myURL.params;   // = Object = { id: 255, m: hello }
  myURL.path;     // = '/dir/index.html'
  myURL.segments; // = Array = ['dir', 'index.html']
  myURL.port;     // = '8080'
  myURL.protocol; // = 'http'
  myURL.source;   // = 'http://abc.com:8080/dir/index.html?id=255&m=hello#top'
</script>
```

#### AMD
```html
<script>
require(['bower_components/dom-url-parser'], function (domUrl) {
  var myURL = domUrl('http://abc.com:8080/dir/index.html?id=255&m=hello#top');
});
</script>
```