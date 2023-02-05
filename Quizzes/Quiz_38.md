## Code
```.py
import random
import matplotlib.pyplot as plt
random.seed(1234)



class coordinate:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __repr__(self)->str:
        return f"[Coordinate object] x:{self.x}, y:{self.y}"

class city:
    def __init__(self, name:str, location:coordinate):
        self.name = name
        self.location = location

    def __repr__(self)->str:
        return f"[City Object] City {self.name} is located at {self.location}"

    def distance(self, cityB):
        xa, ya = self.location.x, self.location.y
        xb,yb = cityB.location.x, cityB.location.y

        d = ((xa - xb)**2 + (ya - yb)**2) ** (1/2)
        return round(d, 2)

class country:
    def __init__(self, name:str):
        self.name = name
        self.cities = []

    def add_city(self, new_city:city):
        self.cities.append(new_city)

    def __repr__(self)->str:
        return f"[Country Object] The name of the country is {self.name.title()} and it has {len(self.cities)} cities"

point1 = coordinate(x=5, y=5)
print(point1)
Tokyo = city(name="tokyo", location=point1)
Kyoto = city(name="kyoto", location=coordinate(x=10, y=10))

Japan = country(name="Japan")

for name in ["Tokyo", "Yokahoma", "Osaka", "Nagoya", "Sapporo", "Kobe", "Kyoto", "Fukuoka", "Kawasaki", "Saitama"]:
    rand_loc = coordinate(x=random.randint(0, 100), y=random.randint(0,100))
    ct = city(name=name, location = rand_loc)
    Japan.add_city(ct)

# distance from tokyo to any other
for city in Japan.cities:
    d = Japan.cities[0].distance(cityB=city)
    print(f"Distance between {Japan.cities[0].name} and {city.name} is {d}")

    plt.scatter(city.location.x, city.location.y, color="red")
    plt.text(city.location.x, city.location.y, city.name)


    plt.xlabel("Distance km")
    plt.ylabel("Distance km")

total_distance = 0

plt.show()
```
## Scatter Plot
<img width="368" alt="Screen Shot 2023-02-05 at 14 20 54" src="https://user-images.githubusercontent.com/111941990/216803143-9ff87d8f-9066-48fb-a524-8bcae5083ef2.png">

## Code
```.py
import random
import matplotlib.pyplot as plt
random.seed(1234)



class coordinate:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __repr__(self)->str:
        return f"[Coordinate object] x:{self.x}, y:{self.y}"

class city:
    def __init__(self, name:str, location:coordinate):
        self.name = name
        self.location = location

    def __repr__(self)->str:
        return f"[City Object] City {self.name} is located at {self.location}"

    def distance(self, cityB):
        xa, ya = self.location.x, self.location.y
        xb,yb = cityB.location.x, cityB.location.y

        d = ((xa - xb)**2 + (ya - yb)**2) ** (1/2)
        return round(d, 2)

class country:
    def __init__(self, name:str):
        self.name = name
        self.cities = []

    def add_city(self, new_city:city):
        self.cities.append(new_city)

    def __repr__(self)->str:
        return f"[Country Object] The name of the country is {self.name.title()} and it has {len(self.cities)} cities"

point1 = coordinate(x=5, y=5)
print(point1)
Tokyo = city(name="tokyo", location=point1)
Kyoto = city(name="kyoto", location=coordinate(x=10, y=10))

Japan = country(name="Japan")

for name in ["Tokyo", "Yokahoma", "Osaka", "Nagoya", "Sapporo", "Kobe", "Kyoto", "Fukuoka", "Kawasaki", "Saitama"]:
    rand_loc = coordinate(x=random.randint(0, 100), y=random.randint(0,100))
    ct = city(name=name, location = rand_loc)
    Japan.add_city(ct)

# distance from tokyo to any other
for city in Japan.cities:
    d = Japan.cities[0].distance(cityB=city)
    print(f"Distance between {Japan.cities[0].name} and {city.name} is {d}")

    plt.scatter(city.location.x, city.location.y, color="red")
    plt.text(city.location.x, city.location.y, city.name)


    plt.xlabel("Distance km")
    plt.ylabel("Distance km")

total_distance = 0
for i in range(0, len(Japan.cities)-1):
    start_city = Japan.cities[i]
    end_city = Japan.cities[i+1]
    x = [start_city.location.x, end_city.location.x]
    y = [start_city.location.y, end_city.location.y]
    plt.plot(x, y, color = "blue")
    d = start_city.distance(cityB=end_city)
    total_distance += d
plt.show()
```

## Distance Graph
<img width="370" alt="Screen Shot 2023-02-05 at 14 29 18" src="https://user-images.githubusercontent.com/111941990/216803390-a8e9b874-5043-499b-9729-fad4789b485f.png">

## Pycharm
<img width="757" alt="Screen Shot 2023-02-05 at 14 30 35" src="https://user-images.githubusercontent.com/111941990/216803510-d84d7f20-c662-4ffc-bdd8-7df59f1277d8.png">

<img width="959" alt="Screen Shot 2023-02-05 at 14 30 49" src="https://user-images.githubusercontent.com/111941990/216803524-6deedab2-eeb2-47f2-9d74-195703c4ad51.png">

<img width="464" alt="Screen Shot 2023-02-05 at 14 30 56" src="https://user-images.githubusercontent.com/111941990/216803534-ad16b362-e836-441e-b852-8ee1679e512c.png">



