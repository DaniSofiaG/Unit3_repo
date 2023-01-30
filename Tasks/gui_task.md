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


# Gui Task
## Python Code
```.py
from kivymd.app import MDApp

class converter(MDApp):
    def build(self):
        return

    def __init__(self, **kwargs):
        super().__init__(**kwargs)
        self.home_value = 0

    def jpy(self):
        jpy_value = self.home_value * 6.92
        self.root.ids.value_label.text = f"{self.home_value} MXN pesos is equal {jpy_value} JPY"

    def usd(self):
        # decrease the counter by one and show it in the text of counter_label
        usd_value = self.home_value * 0.53
        self.root.ids.value_label.text = f"{self.home_value} MXN pesos is equal {usd_value} USD"

    def set_home_value(self):
        number = int(self.root.ids.user_num.text)
        self.home_value = number
        self.root.ids.value_label.text = f"Count is {self.set_home_value()}"

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

            MDRaisedButton:
                text: "CLICK TO CONVERT"
                pos_hint: {"center_x": 0.5, "center_y":0.9}
                md_bg_color: "#00C2D1" #aqua blue

            MDBoxLayout:
                id: space_box
                orientation: "horizontal"
                size_hint: 2.1, 0.3

            MDBoxLayout:
                id: fourth_box
                orientation: "horizontal"
                size_hint: 1, 1


                MDRaisedButton:
                    text: "JPY"
                    md_bg_color: "red"
                    pos_hint: {"center_x": 0.5, "center_y":0.9}
                    on_release:
                        app.jpy()


                MDRaisedButton:
                    text: "USD"
                    md_bg_color: "blue"
                    pos_hint: {"center_x": 0.5, "center_y":0.9}
```

## Evidence
<img width="942" alt="Screen Shot 2023-01-29 at 22 43 32" src="https://user-images.githubusercontent.com/111941990/215330184-a564acde-3587-4c82-8726-d64e561c4a9f.png">
