Since PhantomJS is based on [QtWebKit](http://doc.qt.nokia.com/4.8-snapshot/qtwebkit-guide.html), it basically supports whatever features shipped in the module. For Qt version 4.8, it is equivalent to QtWebKit 2.2, see the its list of [all features](http://trac.webkit.org/wiki/QtWebKitFeatures22) for more information.

## Detecting Features

Using WebKit version and compare it against other WebKit-based browser is not encouraged. The reason is because every WebKit implementation may have varying support due to its architecture of having [interface/ abstraction layer](http://ariya.ofilabs.com/2011/06/your-webkit-port-is-special-just-like-every-other-port.html).

The best way to find out if a certain feature is supported or not is via feature detection, for example by using a library like [Modernizr](http://www.modernizr.com/docs/#s2). The included `examples/features.js` illustrates the use of Modernizr and dumps all the detected features, both supported and not supported.

Please note that although a certain feature might be supported, there is no really guarantee that it is 100% supported. You still have run your own extensive tests to make sure that the support level is up to what you need.

## Irrelevant Features

The following features, due to the nature of PhantomJS, are irrelevant. They may or may not be supported in any future version.

WebGL would require OpenGL-capable system. Since the goal of PhantomJS is to become 100% headless and self-contained, this is not acceptable. Using OpenGL emulation via Mesa can overcome the limitation, but then the performance would degrade.

**Video and Audio** would require shipping a variety of different codecs implementation.

**CSS 3-D** Transformation needs a perspective-correct implementation of texture mapping. It can't be implemented with a penalty in performance.

**Plugins** such as Flash, Silverlight, etc are platform-dependent. They may also require native window handle, something which PhantomJS can not always provide by being headless.

Each of the above feature needs to be evaluated on a case-by-case to see whether it is suitable to be included or not. Until then, do not rely on them.

## Not Tested Features

XPath.