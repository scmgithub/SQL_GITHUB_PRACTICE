#SQL and GitHub practice

To create receipts table:
```create table receipts (id INTEGER PRIMARY KEY, store TEXT, item TEXT, number_of_items INTEGER, price REAL, buy_date TEXT);```

All the attributes from all the receipts
```select * from receipts;```

The store and item names from all the receipts
```select store, item from receipts;```

All the attributes from all purchases made at Toys R Us
```select * from receipts where store = "Toys R Us";```

The item name of each purchase made at Strand.
```select item from receipts where store = "Strand";```

The total number of items Peter purchased
```select sum(number_of_items) from receipts;```

The total number of items purchased at Sears
```select count(number_of_items) from receipts where store="Sears";```

All the attributes of receipts where Peter bought multiple items.
Q7**answer**

The average number of items purchased on a trip to JC Penny
Q8**answer**

Great, now add a new receipt representing the purchase of a single "Heatstreet Maple Bourbon", purchased for $40.99 at "Schnapps Haus" on the most recent fourth of July.
Q9**answer**
