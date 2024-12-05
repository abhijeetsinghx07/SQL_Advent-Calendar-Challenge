**Question level of difficulty: Hard**


> You’re trying to identify the most calorie-packed candies to avoid during your holiday binge. Write a query to rank candies based on their calorie count within each category. Include the candy name, category, calories, and rank (rank_in_category) within the category.

Table name: candy_nutrition

```sql
| candy_id | candy_name              | calories | candy_category |
|----------|-------------------------|----------|----------------|
| 1        | Candy Cane              | 200      | Sweets         |
| 2        | Chocolate Bar           | 250      | Chocolate      |
| 3        | Gingerbread Cookie      | 150      | Baked Goods    |
| 4        | Lollipop                | 100      | Sweets         |
| 5        | Dark Chocolate Truffle  | 180      | Chocolate      |
| 6        | Marshmallow             | 900      | Sweets         |
| 7        | Sugar Cookie            | 140      | Baked Goods    |


```

```sql
SELECT candy_name, candy_category, calories,
    RANK() OVER (PARTITION BY candy_category ORDER BY calories DESC) AS rank_in_category
FROM candy_nutrition;
```