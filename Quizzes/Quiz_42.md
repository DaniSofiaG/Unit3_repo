# Quiz 42
<img width="783" alt="Screen Shot 2023-03-13 at 9 10 46" src="https://user-images.githubusercontent.com/111941990/224582735-01ece24e-12f8-4cc3-a815-6e664b436d3e.png">

## Python file
```.py
from kivymd.app import MDApp
from kivymd.uix.screen import MDScreen


class mystery(MDApp):
    def build(self):
        return


class MysteryPageA(MDScreen):
    pass


class MysteryPageB(MDScreen):
    pass


test = mystery()
test.run()
```

## Kivy file

```.py
ScreenManager:
    id: scr_manager
    MysteryPageA:
        name:"MysteryPageA"
    MysteryPageB:
        name: "MysteryPageB"

<MysteryPageA>:
    MDLabel:
        text: "This is mystery page A you pressed the button"
        size_hint: 1, .1
        halign: "center"
        pos_hint: {"center_x":.5, "center_y":.5}

    MDRaisedButton:
        size_hint: .5, .1
        text: "Next"
        md_bg_color: "#e63946"
        on_release: app.root.current = "MysteryPageB"

<MysteryPageB>:
    MDLabel:
        text: "This is mystery page B you pressed the button"
        size_hint: 1, .1
        halign: "center"
        pos_hint: {"center_x":.5, "center_y":.5}

    MDRaisedButton:
        size_hint: .5, .1
        text: "Back"
        halign: "center"
        md_bg_color: "#e63946"
        on_release: app.root.current = "MysteryPageA"
```

## Evidence Recording
https://user-images.githubusercontent.com/111941990/224582845-b44df113-595f-4bc0-8c9a-0d57f8489ca1.mov


