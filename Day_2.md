**Question level of difficulty: Easy**

> Santa wants to know which gifts weigh more than 1 kg. Can you list them?

**Table name: gifts**

```sql
| Gift Name       | Recipient | Weight (kg) |
|------------------|-----------|-------------|
| Toy Train        | John      | 2.5         |
| Chocolate Box    | Alice     | 0.8         |
| Teddy Bear       | Sophia    | 1.2         |
| Board Game       | Liam      | 0.9         |
```

```sql
SELECT gift_name
FROM gifts
WHERE  weight_kg > 1;
```
