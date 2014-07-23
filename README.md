#Fred
Basically the same thing as https://github.com/reonomy/node-fred
for browser usage (request Mikeal's request with jQuery)

![FRED Logo](http://research.stlouisfed.org/images/fred-logo-2x.png)

### Usage
```
<script type="text/javascript" src="//cdnjs.cloudflare.com/ajax/libs/jquery/2.1.1/jquery.js"></script>
<script type="text/javascript" src="fred.js"></script>
```

### API Key
Fred and the FRED API require and API key. You can [request an api key from the official Federal Reserve web site](http://api.stlouisfed.org/api_key.html).

### Overview

Create an instance of `fred` with your API key:
```javascript
var fred = Fred('GiVeMe1APIKeYPLeaSe');
```

Request a resource:
```javascript
fred.series.observations('GDP', function(err, grossNationalProduct) {
  if (!err) console.log(grossNationalProduct.observations)
});
```


### More information

The [documentation for the FRED API](http://api.stlouisfed.org/docs/fred/#General_Documentation) is available on the Federal Reserve's web site.
