
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
      image = __dirname + '/love-letter.jpg';

    // detectType: `LocateRecognize`代表整图文字检测、识别,以行为单位（默认）  
    // languageType: `CHN_ENG`(中英)（默认）  
    // imageType: `2`代表图片原文件（只支持JPG）  
    // image: 图片路径  
    ocr.scan( 'LocateRecognize', 'CHN_ENG', 2, image, function( err, data ) {
      if ( err ) {
        return console.error( err );
      }

      console.log( 'words:' );
      console.log( data.word );
    });

实测
===========

识别率几乎100%

![启示录](https://github.com/JeremyWei/baidu-ocr/blob/master/test/001.jpg)

```
公司投入宝贵的时间和金钱之前，淘汰蹩脚的创意，找出对公司最有利的机会。产品的机会评估结果出来后，别忘了呈报给公司高管，与高管讨论，决定是否开发此产品。如果决定继续开发，了解高管的想法，有助于你尔进一步开展工作。如果cEo告诉你不管愿不愿意，都要继续开发，该怎么办？在这种情况下，迅速进行机会评估，明确产品需求也是必要的你得到的结论可能会改变CEO的看法，即使不能，至少你能明确产品目标，大大提高产品成功的可能性。
```

LICENSE
===========
The MIT License (MIT)
Copyright (c) 2014 Jeremy Wei

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.