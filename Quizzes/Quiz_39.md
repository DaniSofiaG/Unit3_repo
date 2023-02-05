## Code
from kivymd.app import MDApp


class adding(MDApp):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)
        self.count = 0

    def build(self):
        return

    def set_counter(self):
        # validate that it is a digit
        self.root.ids.count_label.text = f"Count {self.count}"

    def add(self, name: str):
        if 'up' in name:
            self.count += 1
        self.root.ids.count_label.text = f"Count {self.count}"


counter = adding()
counter.run()


## KV
```.py
Screen:
    size: 500, 500

    MDBoxLayout:
        id: main_box
        orientation: "horizontal" #organized vertically
        size_hint: .7, .3
        md_bg_color: "#F5B700"
        pos_hint:{"center_x":.5, "center_y":.5}

        MDLabel:
            id: count_label
            font_style: "H3"
            halign: "center"
            font_size: '34pt'

        MDRaisedButton:
            id: add_btn
            md_bg_color: "#DC0073"
            text: "Add +1"
            on_press: app.add("up")
            size_hint: 1,1
            font_size: '34pt'
```



https://user-images.githubusercontent.com/111941990/216804073-079d43c3-1586-4d4f-ac21-4c9fb499337d.mov

