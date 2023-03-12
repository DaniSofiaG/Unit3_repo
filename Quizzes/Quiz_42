# Quiz 42

# mystery.kv

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
