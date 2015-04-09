#SQL and GitHub practice

To create receipts table:
```sql
create table receipts (id INTEGER PRIMARY KEY, store TEXT, item TEXT, number_of_items INTEGER, price REAL, buy_date TEXT);
```

All the attributes from all the receipts
```sql
select * from receipts;
```

The store and item names from all the receipts
```sql
select store, item from receipts;
```

All the attributes from all purchases made at Toys R Us
```sql
select * from receipts where store = "Toys R Us";
```

The item name of each purchase made at Strand.
```sql
select item from receipts where store = "Strand";
```

The total number of items Peter purchased
```sql
select sum(number_of_items) from receipts;
```

The total number of items purchased at Sears
```sql
select count(number_of_items) from receipts where store="Sears";
```

All the attributes of receipts where Peter bought multiple items.
```sql
select * from receipts where number_of_items > 1;
```

The average number of items purchased on a trip to JC Penny
```sql
select avg(number_of_items) from receipts where store = "JC Penny";
```

Great, now add a new receipt representing the purchase of a single "Heatstreet Maple Bourbon", purchased for $40.99 at "Schnapps Haus" on the most recent fourth of July.
```sql
insert into receipts (store, item, number_of_items, price, buy_date) values ("Schnapps Haus", "Heatstreet Maple Bourbon", 1, 40.99, "July 4 2014");
```
