[Back](README.md)

## Forensic 100 p - rudolf

Provided is a file with loads of numbers in it.

These are just decimals and after converting from decimals to raw, it reveals a PNG header so we try to render the image.
![example](images/forensic/rudolfcyber.png)
![example](images/forensic/rudolfsol.png)

Flag: *NC3{JULERENSDYR!}*

---

## Forensic 200 p - Zip-Mareridt!!!



---

## Forensic 350 p - indrammet_julemand

Again provided file are just decimals after conversion we're left with alot of data.
![example](images/forensic/indrammet_rick.png)

The rebrand link is just an easter egg, rick can be found every year.

I went straight into using `binwalk` to examine the file:

![example](images/forensic/indrammet_binwalk.png)

after inspecting the image `binwalk` extracted.
It was a classic `stegsolve` opportunity:

![example](images/forensic/stegsolve_indrammet.png)

Flag: *NC3{JULEMANDENS_RENSDYR_På_TUR}*

---

[Back](README.md)