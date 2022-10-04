# PYTHON File
````
# program-challenge02.py
from pyzbar import pyzbar
from PIL import Image
#load qr code imge
b = []
for a in range(936):
  image = Image.open(f"challenge{a:04d}.png")
  qr_code = pyzbar.decode(image)[0]
  data= qr_code.data.decode("utf-8")
  type = qr_code.type
  text = f"{data}"
  b.append(chr(int(text)))
print("".join(b))
````

# 
