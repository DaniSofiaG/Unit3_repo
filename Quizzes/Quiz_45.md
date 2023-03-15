# Quiz 45

<img width="995" alt="Screen Shot 2023-03-15 at 17 49 08" src="https://user-images.githubusercontent.com/111941990/225256080-0f1f3284-13dc-4eab-9ecf-6effe0f493ff.png">

## UML Diagram
![Untitled drawing (3)](https://user-images.githubusercontent.com/111941990/225371247-4129b047-054b-48af-bdc4-323942a9c823.png)


## SQL
```.py
SELECT * from accounts;
SELECT * from customers;
SELECT * from transactions;
SELECT sum(amount) from transactions GROUP by account_id;
SELECT transactions.account_id, accounts.account_id, accounts.balance, sum(transactions.amount)  from transactions INNER JOIN accounts ON transactions.account_id = accounts.account_id WHERE transactions.transaction_type = "deposit" GROUP BY transactions.account_id;
SELECT account_id, transaction_type, sum(amount) from transactions;
SELECT sum(amount) AS deposits from transactions WHERE transaction_type="deposit" GROUP by account_id;
SELECT sum(amount) AS withdrawls from transactions WHERE transaction_type="withdraw" GROUP by account_id;
ALTER TABLE transactions ADD deposits;
ALTER TABLE transactions ADD withdrawls;
```
<img width="1440" alt="Screen Shot 2023-03-16 at 2 26 23" src="https://user-images.githubusercontent.com/111941990/225391642-b749c10f-98b4-4d5a-a9bc-21ecdd7b6932.png">


