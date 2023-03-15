# Quiz 48
<img width="410" alt="Screen Shot 2023-03-15 at 17 03 19" src="https://user-images.githubusercontent.com/111941990/225245454-0467a991-b202-4a36-80fd-5acf5ef50b01.png">

## Python File
```.py
import sqlite3
from secure_password import encrypt_password, check_password, pwd_config

class database_worker:
    def __init__(self, name):
        self.connection = sqlite3.connect(name)
        self.cursor = self.connection.cursor()

    def search(self, query):
        result = self.cursor.execute(query).fetchall()
        return result

    def run_save(self, query):
        self.cursor.execute(query)
        self.connection.commit()

    def close(self):
        self.connection.close()


x = database_worker("bitcoin_exchange.db")
query = "SELECT * from ledger"
result = x.search(query)
print(result)
x.close()


for row in result:
    id = row[0]
    sender_id = row[1]
    receiver_id = row[2]
    amount = row[3]
    hash = row [4]
    string_hash = f"id {id},sender_id {sender_id},receiver_id {receiver_id},amount {amount}"

    if check_password(hashed_password = hash, user_password = string_hash):
        print(f"Tx(id={id})Signature matches")
    else:
        print(f"Tx(id={id}Error signature")
```

## Evidence 
<img width="1337" alt="Screen Shot 2023-03-15 at 17 07 21" src="https://user-images.githubusercontent.com/111941990/225246139-f5a13157-eb25-4e1a-9245-a0b70a9df520.png">


        
