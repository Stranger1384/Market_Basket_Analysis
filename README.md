# Market_Basket_Analysis
## Dataset Description
- Groceries dataset containing over 38k items
- each item has `Member_number` associated with it, Which can be used to make Baskets
## Libraries used:
- numpy (as np)
- pandas
- matplotlib
- mlxtend

## Plot most frequent items:
![6cad79b6-1410-4387-85dc-a710c8987c9c](https://github.com/Stranger1384/Market_Basket_Analysis/assets/117520926/ce91fb06-ae79-406e-8b54-79c9903c10e4)

## Apriori Algorithm:
- Set the minimum support `min_support` as `0.02`
```
freq_items = apriori(X, min_support=0.02, use_colnames=True)
```
## Derived Association rules:
- kept minimum threshold for support `min_threshold` as `0.05`
```
rules = association_rules(freq_items, metric = 'support', min_threshold = 0.05)
```
-After filtering number of rules Generated : `28`

## Generated rules: 
```
bottled water -->  other vegetables 
bottled water -->  rolls/buns 
bottled water -->  soda 
bottled water -->  yogurt 
rolls/buns -->  other vegetables 
other vegetables -->  rolls/buns 
root vegetables -->  other vegetables 
sausage -->  other vegetables 
soda -->  other vegetables 
other vegetables -->  soda 
tropical fruit -->  other vegetables 
yogurt -->  other vegetables 
other vegetables -->  yogurt 
root vegetables -->  rolls/buns 
sausage -->  rolls/buns 
soda -->  rolls/buns 
rolls/buns -->  soda 
tropical fruit -->  rolls/buns 
yogurt -->  rolls/buns 
rolls/buns -->  yogurt 
root vegetables -->  soda 
root vegetables -->  yogurt 
sausage -->  soda 
sausage -->  yogurt 
tropical fruit -->  soda 
soda -->  yogurt 
yogurt -->  soda 
tropical fruit -->  yogurt 
```

## Converted these Rules to Basket:
```
['rolls/buns', 'bottled water']
['sausage', 'other vegetables']
['root vegetables', 'other vegetables']
['rolls/buns', 'other vegetables']
['sausage', 'rolls/buns']
['yogurt', 'rolls/buns']
['yogurt', 'root vegetables']
['soda', 'rolls/buns']
['rolls/buns', 'root vegetables']
['tropical fruit', 'soda']
['tropical fruit', 'rolls/buns']
['yogurt', 'sausage']
['soda', 'bottled water']
['bottled water', 'other vegetables']
['soda', 'other vegetables']
['soda', 'root vegetables']
['soda', 'sausage']
['tropical fruit', 'other vegetables']
['tropical fruit', 'yogurt']
['yogurt', 'other vegetables']
['soda', 'yogurt']
['yogurt', 'bottled water']
```

## References:
1. https://www.simplilearn.com/tutorials/machine-learning-tutorial/apriori-algorithm-in-data-mining
2. Dataset obtained from [Kaggle](https://www.kaggle.com/).
