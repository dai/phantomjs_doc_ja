# スクリーンキャプチャー

PhantomJSは実際のレイアウトとレンダリングエンジンのWebKitを使っているので、スクリーンショットのようにWebページをキャプチャーすることができます。PhantomJSはWebページ上のどんなものでもレンダリングできるので、HTMLやCSSの内容だけでなくSVGやCanvasの内容も変換することができます。
<!-- Since PhantomJS is using WebKit, a real layout and rendering engine, it can capture a web page as a screenshot. Because PhantomJS can render anything on the web page, it can be used to convert contents not only in HTML and CSS, but also SVG and Canvas. -->

次のスクリプトは、最も簡単なページキャプチャーの使用方法を示しています。Githubのホームページをロードして、それを画像として`github.png`で保存します 。
<!-- The following script demonstrates the simplest use of page capture. It loads the Github homepage and then saves it as an image, `github.png`. -->

```javascript
var page = require('webpage').create();
page.open('http://github.com/', function () {
    page.render('github.png');
    phantom.exit();
});
```

PhantomJSは、PNG形式の他にJPEG、GIF、PDFファイルをサポートしています。
<!-- Beside PNG format, PhantomJS supports JPEG, GIF, and PDF. -->

サブディレクトリの`examples`には、PhantomJSのより完全なレンダリング機能を示している[rasterize.js](https://github.com/ariya/phantomjs/blob/master/examples/rasterize.js)（30行）スクリプトがあります。有名なタイガー（SVG）のレンダリングを生成する例:
<!-- In the `examples` subdirectory, there is a script [rasterize.js](https://github.com/ariya/phantomjs/blob/master/examples/rasterize.js) (30 lines) which demonstrates a more complete rendering feature of PhantomJS. An example to produce the rendering of the famous Tiger (from SVG): -->

```
phantomjs rasterize.js http://ariya.github.com/svg/tiger.svg tiger.png
```

次の`tiger.png`のようになります:
<!-- which gives the following `tiger.png`: -->

![Rendered Tiger](http://lh6.ggpht.com/_Oijhf1ZPv-4/TR6iM8J0KrI/AAAAAAAABy4/RCZ8Eg567LM/s400/tiger.png)

別の例は、[polar clock](http://raphaeljs.com/polar-clock.html)（RaphaelJS）を表示します:
<!-- Another example is to show [polar clock](http://raphaeljs.com/polar-clock.html) (from [RaphaelJS](http://raphaeljs.com)): -->

```
phantomjs rasterize.js http://raphaeljs.com/polar-clock.html clock.png
```
![Polar Clock](https://lh5.googleusercontent.com/_Oijhf1ZPv-4/TUuUx1o-tuI/AAAAAAAAB00/Ba-Gxl5Zp6Q/s288/polar-clock.png)

PDF出力の生成も簡単です。次はWikipediaの記事からの例になります:
<!-- Producing PDF output is also easy, e.g. from a Wikipedia article: -->

```
phantomjs rasterize.js 'http://en.wikipedia.org/w/index.php?title=Jakarta&printable=yes' jakarta.pdf
```

Canvasは簡単に構築され、画像に変換されます。含まれているサンプルの[colorwheel.js](https://github.com/ariya/phantomjs/blob/master/examples/colorwheel.js)（50行）は、次のカラーホイールを生成します:
<!-- Canvas can be easily constructed and converted to an image. The included example [colorwheel.js](https://github.com/ariya/phantomjs/blob/master/examples/colorwheel.js) (50 lines) produces the following color wheel: -->

![Color Wheel](https://lh3.googleusercontent.com/-xSIzxPtJULw/TVzeP4NPMDI/AAAAAAAAB10/k-c8jB6I5Cg/s288/colorwheel.png)

PhantomJSを使用することで、Webのスクリーンショットサービスを構築することが可能です。[some projects](./Related-Projects.md)にあるようなサービスを作成することが容易になります。PhantomJSベースのスクリーンショットサービスの例としては、 [Screener](http://screener.brachium-system.net)と[ChromaNope](http://chromanope.com/)があります。
<!-- It is possible to build a web screenshot service using PhantomJS. There are [[some projects|Related Projects]] which make it easy to create such a service. Examples of PhantomJS-based screenshot services are [Screener](http://screener.brachium-system.net) and [ChromaNope](http://chromanope.com/). -->