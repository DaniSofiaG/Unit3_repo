# Example 1

## Python Code
```.py
from kivymd.app import MDApp

class example1(MDApp):
    def build(self):
        return
        
test = example1()
test.run()
```

## KV File

```.py
Screen:
    size: 500, 500

    MDLabel:
        text: "Hello World"
        halign: "center"
        font_size: "34pt"
```

## Evidence
<img width="845" alt="Screen Shot 2023-01-29 at 22 46 06" src="https://user-images.githubusercontent.com/111941990/215330333-b57e5d89-fc67-4bc0-bd95-52b22e37fe1b.png">


# Example 2
## Python Code
```.py
from kivymd.app import MDApp

class example2(MDApp):
    def build(self):
        return

    def close(self):
        exit()

test = example2()
test.run()
```

## KV File
```.py
# example2.kv
Screen:
    size: 500, 500
    MDBoxLayout:
    pos_hint: {"center_x":0.5}
    size_hint: .7, .7
    md_bg_color: "#fdfcdc"
    orientation: "vertical"

    MDLabel:
        text: "Hello World"
        halign: "center"
        font_size: "34pt"

    MDRaisedButton:
        text: "Close"
        size_hint: .5, .4
        font_size: "34pt"
        md_bg_color: "#f07167"
        pos_hint: {"center_x":0.5}
        on_press:
            app.close()
```


## Evidence
<img width="806" alt="Screen Shot 2023-01-30 at 10 18 52" src="https://user-images.githubusercontent.com/111941990/215368511-98c716c0-34a6-4c96-95b2-7f614c86a430.png">

# Example 3
## Python Code
```.py
from kivymd.app import MDApp


class example3(MDApp):
    def build(self):
        return

    def change_author(self, name):
        self.root.ids.title.text = f"Author {name}"

exam = example3()
exam.run()
```

## KV File
```.py
Screen:
    size: 500, 500
    MDLabel:
        id: title
        text: ""
        font_style: "H1"
        pos_hint: {"center_y":.8}
        halign: "center"

    MDBoxLayout:
        pos_hint: {"center_x":.5,"center_y":.5}
        size_hint: .7, .2
        orientation: "horizontal"

        MDChip:
            text: "Author A"
            pos_hint: {"center_y": .5}
            icon_right: "close-circle-outline"
            md_bg_color: "#003049"
            text_color: "#FFFFFF"
            on_press: app.change_author("A")

        MDChip:
            text: "Author B"
            pos_hint: {"center_y": .5}
            icon_right: "close-circle-outline"
            md_bg_color: "#D62828"
            on_press: app.change_author("B")

        MDChip:
            text: "Author C"
            pos_hint: {"center_y":.5}
            icon_right: "close-circle-outline"
            md_bg_color: "#F77F00"
            on_press: app.change_author("C")

        MDChip:
            text: "Author D"
            pos_hint: {"center_y":.5}
            icon_right: "close-circle-outline"
            md_bg_color: "#FCBF49"
            on_press: app.change_author("D")

        MDChip:
            text: "Author E"
            pos_hint: {"center_y":.5}
            icon_right: "close-circle-outline"
            md_bg_color: "#EAE2B7"
            on_press: app.change_author("E")
```
## Evidence

<img width="811" alt="Screen Shot 2023-01-30 at 19 15 06" src="https://user-images.githubusercontent.com/111941990/215449895-65c08022-8562-4823-a6fd-79b62ede5e38.png">

# Gui Task
## Python Code
```.py
import sys
sys.setrecursionlimit(10**6)

from kivymd.app import MDApp

class converter(MDApp):
    def build(self):
        return

    def __init__(self, **kwargs):
        super().__init__(**kwargs)
        self.home_value = 0

    def jpy(self):
        self.home_value * 6.92
        self.root.ids.jpy_value.text = f"¥{round(self.home_value * 6.92, 2)} JPY"

    def usd(self):
        self.home_value * 0.53
        self.root.ids.jpy_value.text = f"${round(self.home_value / 18.77, 2)} USD"

    def set_home_value(self):
        number = int(self.root.ids.user_num.text)
        self.home_value = number

test = converter()
test.run()
```

## KV File
```.py
Screen:
    size: 500, 500

    MDBoxLayout:
        id: first_holder_box
        orientation: "vertical"
        size_hint: 1, 1 #percentages on the screen
        pos_hint: {"center_x": 0.5}
        md_bg_color: "#FCDC4D" #yellow

        MDLabel:
            text: "Currency Converter"
            halign: "center"
            font_size: "20pt"

        MDBoxLayout:
            id: first_box
            orientation: "vertical"
            size_hint: 0.7, 0.2
            pos_hint: {"center_x": 0.5}
            md_bg_color: "#E9E3E6" #white

            MDTextField:
                id: user_num
                hint_text: "MXN Pesos: "
                helper_text: "This will disappear when you click off"
                helper_text_mode: "on_focus"
                on_text:
                    app.set_home_value()

        MDBoxLayout:
            id: second_holder_box
            orientation: "horizontal"
            size_hint: 0.7, 1
            pos_hint: {"center_x": 0.5}

            MDLabel:
                text: "CLICK TO CONVERT"
                pos_hint: {"center_x": 0.5, "center_y":0.9}
                size_hint: 0.9, 0.3
                font_size: 35

            MDBoxLayout
                id: space_box_3
                orientation: "horizontal"
                size_hint: 1, 0.5
                pos_hint: {"center_y":0.9}



            MDBoxLayout:
                id: fourth_box
                orientation: "horizontal"
                size_hint: 1, 1


                MDRaisedButton:
                    id: jpy_value
                    text: "JPY"
                    md_bg_color: "red"
                    pos_hint: {"center_x": 0.5, "center_y":0.9}
                    on_release:
                        app.jpy()


                MDRaisedButton:
                    id: usd_value
                    text: "USD"
                    md_bg_color: "blue"
                    pos_hint: {"center_x": 0.5, "center_y":0.9}
                    on_release:
                        app.usd()
```

## Evidence
<img width="816" alt="Screen Shot 2023-01-30 at 14 05 16" src="https://user-images.githubusercontent.com/111941990/215391906-b02c8416-2d84-4bdd-8bb6-125e224b1d47.png">

https://user-images.githubusercontent.com/111941990/215391305-8ac2e345-35e7-4683-afba-2cb2f6d4b5f9.mov

