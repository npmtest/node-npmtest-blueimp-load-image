# npmtest-blueimp-load-image

#### basic test coverage for  [blueimp-load-image (v2.12.2)](https://github.com/blueimp/JavaScript-Load-Image)  [![npm package](https://img.shields.io/npm/v/npmtest-blueimp-load-image.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-blueimp-load-image) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-blueimp-load-image.svg)](https://travis-ci.org/npmtest/node-npmtest-blueimp-load-image)

#### JavaScript Load Image is a library to load images provided as File or Blob objects or via URL. It returns an optionally scaled and/or cropped HTML img or canvas element. It also provides a method to parse image meta data to extract Exif tags and thumbnails and to restore the complete image header after resizing.

[![NPM](https://nodei.co/npm/blueimp-load-image.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/blueimp-load-image)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-blueimp-load-image/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-blueimp-load-image/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-blueimp-load-image/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-blueimp-load-image/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-blueimp-load-image/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-blueimp-load-image/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-blueimp-load-image/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-blueimp-load-image/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-blueimp-load-image/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-blueimp-load-image/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-blueimp-load-image/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-blueimp-load-image/build/test-report.html](https://npmtest.github.io/node-npmtest-blueimp-load-image/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-blueimp-load-image/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-blueimp-load-image/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-blueimp-load-image/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-blueimp-load-image/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-blueimp-load-image/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-blueimp-load-image/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-blueimp-load-image/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-blueimp-load-image/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "blueimp-load-image",
    "version": "2.12.2",
    "title": "JavaScript Load Image",
    "description": "JavaScript Load Image is a library to load images provided as File or Blob objects or via URL. It returns an optionally scaled and/or cropped HTML img or canvas element. It also provides a method to parse image meta data to extract Exif tags and thumbnails and to restore the complete image header after resizing.",
    "keywords": [
        "javascript",
        "load",
        "loading",
        "image",
        "file",
        "blob",
        "url",
        "scale",
        "crop",
        "img",
        "canvas",
        "meta",
        "exif",
        "thumbnail",
        "resizing"
    ],
    "homepage": "https://github.com/blueimp/JavaScript-Load-Image",
    "author": {
        "name": "Sebastian Tschan",
        "url": "https://blueimp.net"
    },
    "repository": {
        "type": "git",
        "url": "git://github.com/blueimp/JavaScript-Load-Image.git"
    },
    "license": "MIT",
    "devDependencies": {
        "phantomjs-prebuilt": "2.1.13",
        "mocha-phantomjs-core": "1.3.1",
        "standard": "8.3.0",
        "uglify-js": "2.7.3"
    },
    "scripts": {
        "lint": "standard *.js js/*.js test/*.js",
        "unit": "phantomjs node_modules/mocha-phantomjs-core/mocha-phantomjs-core.js test/index.html",
        "test": "npm run lint && npm run unit",
        "build": "cd js && uglifyjs load-image.js load-image-scale.js load-image-meta.js load-image-fetch.js load-image-exif.js load-image-exif-map.js load-image-orientation.js -c -m -o load-image.all.min.js --source-map load-image.all.min.js.map",
        "preversion": "npm test",
        "version": "npm run build && git add -A js",
        "postversion": "git push --tags origin master master:gh-pages && npm publish"
    },
    "main": "js/index.js"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
