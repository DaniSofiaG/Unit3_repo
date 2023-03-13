# Quiz 41
<img width="845" alt="Screen Shot 2023-03-13 at 9 35 05" src="https://user-images.githubusercontent.com/111941990/224584224-d054b077-cfd1-4318-bf00-e10f945b0b93.png">



## Python File
```.py
from kivymd.app import MDApp


class game(MDApp):
    def build(self):
        return


test = game()
test.run()
```

## Kivy File
```.py

Screen:
    size: 600, 600 #width, height

    MDLabel:
        halign: "center"
        text: "Tic Tac Toe by Daniela"
        font_size: 75
        pos_hint: {"center_x":.5, "center_y":.9}


    MDBoxLayout:
        orientation: "horizontal"
        size_hint: 0.6, 0.6 #percentages on the screen
        pos_hint: {"center_x":.5, "center_y":.4}
        md_bg_color: "#FF0000"



        MDBoxLayout:
            orientation: "vertical"
            size_hint: 0.2, 1 #percentages on the screen
            md_bg_color: "#1AC8ED"



            MDRaisedButton
                size_hint: 0.97, 0.1
                md_bg_color: "#E15A97"
                text: "X"
                font_size: 45
                pos_hint: {"center_x":.5, "center_y":.4}
            MDRaisedButton
                size_hint: 0.97, 0.1
                text: "O"
                font_size: 45
                pos_hint: {"center_x":.5, "center_y":.4}
                md_bg_color: "#65B891"
            MDRaisedButton
                size_hint: 0.97, 0.1
                pos_hint: {"center_x":.5, "center_y":.4}
                md_bg_color: "#FFD151"


        MDBoxLayout:
            orientation: "vertical"
            size_hint: 0.2, 1 #percentages on the screen
            md_bg_color: "#1AC8ED"

            MDRaisedButton
                size_hint: 0.97, 0.1
                md_bg_color: "#FFD151"
                pos_hint: {"center_x":.5, "center_y":.4}
            MDRaisedButton
                size_hint: 0.97, 0.1
                pos_hint: {"center_x":.5, "center_y":.4}
                md_bg_color: "#FFD151"
            MDRaisedButton
                size_hint: 0.97, 0.1
                pos_hint: {"center_x":.5, "center_y":.4}
                md_bg_color: "#FFD151"


        MDBoxLayout:
            orientation: "vertical"
            size_hint: 0.2, 1 #percentages on the screen
            md_bg_color: "#FFD151"

            MDRaisedButton
                size_hint: 0.97, 0.1
                md_bg_color: "#FFD151"
                pos_hint: {"center_x":.5, "center_y":.4}
            MDRaisedButton
                size_hint: 0.97, 0.1
                pos_hint: {"center_x":.5, "center_y":.4}
                md_bg_color: "#FFD151"
            MDRaisedButton
                size_hint: 0.97, 0.1
                pos_hint: {"center_x":.5, "center_y":.4}
                md_bg_color: "#FFD151"
```

## Evidence
<img width="804" alt="Screen Shot 2023-03-13 at 9 31 44" src="https://user-images.githubusercontent.com/111941990/224584176-d9f535d9-97e0-4ba6-badc-b4057d42ff0b.png">

