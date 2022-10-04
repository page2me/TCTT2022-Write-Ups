# PYTHON File
````
# program-challenge02.py
from pyzbar import pyzbar
from PIL import Image
b = []
for a in range(936):
  image = Image.open(f"challenge{a:04d}.png")
  qr_code = pyzbar.decode(image)[0]
  data = qr_code.data.decode("utf-8")
  text = f"{data}"
  b.append(chr(int(text)))
print("".join(b))
````

$ python program-challenge02.py | base64 -d | grep -o -E 'tctt2022{(.*?)}'

tctt2022{r3P37i7Iv3_745K5_N33d_4U7Om47IoN}
