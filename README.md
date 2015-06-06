
Baidu-ocr
===========

[百度OCR文字识别](http://apistore.baidu.com/apiworks/servicedetail/146.html)API For Node

Install
===========

	npm install baidu-ocr

Test
===========

	BAIDU_APIKEY='your api key' make test
	
How to use
===========

    var ocr = require('baidu-ocr').create( 'your api key' ),
      image = './love-letter.jpg';

    scan( detectType, languageType, imageType, image, function( err, data ) {
  
    })

    // detectType: LocateRecognize: 整图文字检测、识别,以行为单位（默认）
    // languageType: CHN_ENG(中英)（默认）
    // imageType: 2代表图片原文件（只支持JPG）
    // image: 图片路径

    ocr.scan( 'LocateRecognize', 'CHN_ENG', 2, image, function( err, data ) {
  
    });


LICENSE
===========
The MIT License (MIT)
Copyright (c) 2014 Jeremy Wei

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.