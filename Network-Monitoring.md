Because PhantomJS permits the inspection of network traffic, it is suitable to build various analysis on the network behavior and performance.

All the resource requests and responses can be sniffed using `onResourceRequested` and `onResourceReceived`. A very simple to log every request and response is illustrated in the example script [netlog.js](https://github.com/ariya/phantomjs/blob/master/examples/netlog.js):

```javascript
var page = require('webpage').create();
page.onResourceRequested = function (request) {
    console.log('Request ' + JSON.stringify(request, undefined, 4));
};
page.onResourceReceived = function (response) {
    console.log('Receive ' + JSON.stringify(response, undefined, 4));
};
page.open(url);
````

By collecting the data and reformatting it, another example, [netsniff.js](https://github.com/ariya/phantomjs/blob/master/examples/netsniff.js), exports the network traffic in [HAR format](http://www.softwareishard.com/blog/har-12-spec). Use [HAR viewer](http://www.softwareishard.com/blog/har-viewer) to visualize the result and get the waterfall diagram.

The following shows an examplary waterfall diagram obtained from BBC website:

![Waterfall Diagram](https://lh6.googleusercontent.com/-xoooH5EB6EE/TgnyJ3r9sRI/AAAAAAAAB98/wYJ_VoWED34/s640/bbc-har.png)