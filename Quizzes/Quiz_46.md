# Quiz 46
<img width="1007" alt="Screen Shot 2023-03-15 at 17 46 41" src="https://user-images.githubusercontent.com/111941990/225255351-1c6fa6f8-aaa6-406d-9cef-610c2235f642.png">

## Python file
```.py
import sqlite3

haiku = """Code flows like a stream
Algorithms guide its way
IN silence, it solves"""

#Create a Database with table Words
connection = sqlite3.connect("id_quiz.db")


#Step 2
cursor = connection.cursor()

query = f"""CREATE TABLE if not exists words(
    id INTEGER PRIMARY KEY,
    words text NOT NULL,
    len INTEGER NOT NULL) 
    """


cursor.execute(query)
connection.commit()

for word in haiku.split():
    query = f"INSERT into words (words, len) values('{word}', '{len(word)}')"
    count = len(word)
    cursor.execute(query)
    connection.commit()

avg = f"SELECT AVG(len) from words"
out = cursor.execute(avg).fetchall()

print(f" average world length is {out}")




#Save changes
connection.commit()
connection.close
```

## Evidence
<img width="920" alt="Screen Shot 2023-03-15 at 17 45 42" src="https://user-images.githubusercontent.com/111941990/225255160-b52ef9bb-eeae-41c8-847e-1627e00feaa5.png">
