# PySVGExport
## _SVGExport for Python_
Idea from [svgexport] using for nodejs
### Install via pip
```shell
pip install pysvgexport
```
### Usage
```python
from pysvgexport.svg_export import SVGExport
svg_data = '''
    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xhtml" width="235.6875px"
            height="112.37257096319047px" viewBox="0 0 235.6875 112.37257096319047">
            <defs>
                <style type="text/css">
                    @font-face {
                        font-family: "Aclonica.ttf";
                        src: url("https://printholo.storage.googleapis.com/personalize-fonts/5_1617877490808_Aclonica.ttf") format("truetype");
                    }
                </style>
                <path
                    d="M 29.050328462552656,81.24213909012583 A 120.43422075282764 120.43422075282764 0&#10;    0  1 206.63717153744733,81.24213909012583 Z"
                    id="svg-text" />
            </defs><text>
                <textPath xmlns:xlink="http://www.w3.org/1999/xhtml" xlink:href="#svg-text" lengthAdjust="spacing"
                    fill="#1ebb6a" method="stretch" textLength="199.6875" spacing="auto" xml:space="preserve"
                    style="font-size: 30px; letter-spacing: 0px; font-family: &quot;Aclonica.ttf&quot;;">LALALALA text</textPath>
            </text>
        </svg>
'''
capture_options = {
      "top": 0,
      "left": 0,
      "scale": 20
    }
output_options = {"omitBackground": True}
oqs = SVGExport(svg_data=svg_data, capture_options=capture_options, output_options=output_options)
image = oqs.execute()
```

[svgexport]: <https://github.com/shakiba/svgexport>