# 40.
```diff
Write a program that creates the GUI below:
```
<img width="925" alt="Screen Shot 2023-02-05 at 15 59 36" src="https://user-images.githubusercontent.com/111941990/216806055-ae6280c6-07f0-4093-ae58-e69d4da509f5.png">

## KV
```.py
Screen:
    size: 500, 500

    MDBoxLayout:
        size_hint: 1, 1
        md_bg_color: "#131200"

        MDLabel:
            text: "Dani"
            halign: "center"
            color: "#FDFFFC"
            font_size: "80pt"

        MDRaisedButton:
            text: "Color"
            md_bg_color: "#FFBCB5"
            halign: "center"
```
## KV
```.py
Screen:
    size: 500, 500

    MDBoxLayout:
        size_hint: 1, 1
        md_bg_color: "#FDFFFC"

        MDLabel:
            text: "Dani"
            halign: "center"
            color: "#131200"
            font_size: "80pt"

        MDRaisedButton:
            text: "Color"
            md_bg_color: "#FFBCB5"
            halign: "center"

```
<img width="809" alt="Screen Shot 2023-02-05 at 15 41 23" src="https://user-images.githubusercontent.com/111941990/216805596-7b4345be-02d9-4a7e-bbc9-68606d26502b.png">
<img width="801" alt="Screen Shot 2023-02-05 at 15 54 38" src="https://user-images.githubusercontent.com/111941990/216805897-1a4c4c94-6c14-49c0-b38c-681914e7aab4.png">
