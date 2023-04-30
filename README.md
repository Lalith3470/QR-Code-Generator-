# Python QR Code Generator
Generate QR codes.

A standard install uses pypng to generate PNG files and can also render QR codes directly to the console. A standard install is just:
```
pip install qrcode
pip install image
```
<mark>Usage</mark>
#Usage
From the command line, use the installed qr script:
```
qr "Some text" > test.png
```
#Or in Python, use the make shortcut function:
```
import qrcode
img = qrcode.make('Some data here')
type(img)  # qrcode.image.pil.PilImage
img.save("some_file.png")
```
#Advanced Usage
For more control, use the QRCode class. For example:
```
import qrcode
import image
qr =qrcode.QRCode(
    version=15,  # 15 means the version og the qr code high the number bigger the code image and complicated picture
    box_size=10,  # size of the box where qr code will be displayed
    border=5  # it is the white part of image -- border in all 4 sides with white color

)
data = "https://github.com/Lalith3470"
qr.add_data(data)
qr.make(fit=True)
img = qr.make_image(fill="black", back_color="white")
img.save("test.png")
```
#QR Code for my GitHub

![test](https://user-images.githubusercontent.com/101722978/235346731-3867299a-2714-4f19-bc91-84b6c29d3442.png)
