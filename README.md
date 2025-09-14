# Codectechnologies-Intern-MarketBasketAnalysis
# Market Basket Analysis
This project implements **Market Basket Analysis (MBA)** on a Groceries dataset using the **Apriori and FP-Growth algorithm**.
The goal is to discover frequent itemsets and association rules that reveal customer purchasing patterns. 
These insights can help retailers:
* Increase cross-selling opportunities.
* Improve store layout and product placement.
* Design data-driven promotional campaigns.

## The project includes:
* End-to-end data cleaning and preprocessing.
* Frequent itemset generation and rule mining.
* Visualization of product associations (heatmaps, bar charts, network graphs).
* Actionable business insights with real-world applications.

## Datase Used:
Dataset Source-Kaggle
[**View Groceries Dataset**](https://github.com/khushi9179/Codectechnologies-Intern-MarketBasketAnalysis/blob/main/Groceries_dataset.csv.xlsx)

## Dataset Summary:
* **Shape:** (38,765 rows, 3 columns)
* **Transactions:** 9,835 baskets (customers × dates grouped)
* **Unique members:** 3,898
* **Unique items:** 167

## Tech Stack:
- Python  
- Pandas, Numpy  
- Mlxtend (Apriori, FP-Growth, Association Rules)  
- Seaborn, Matplotlib, NetworkX  

## Steps Performed:
1. **Data Cleaning**
   - Removed missing values  
   - Grouped transactions per customer per day  
2. **Transaction Encoding**
   - Converted list of transactions into one-hot encoded dataframe  
3. **Frequent Itemsets**
   - Extracted itemsets using **Apriori** and **FP-Growth**  
4. **Association Rules**
   - Generated rules with **support, confidence, and lift**  
5. **Visualization**
   - Top 10 frequent itemsets (bar chart)  
   - Scatter plot (support vs confidence, lift as color)  
   - Network graph of top rules  

## Association Rules (Top Results):
* **(sausage) → (bottled beer)**
  * Confidence: `0.055` (5.5%)
  * Lift: `1.22` → Slight positive association.

* **(frankfurter) → (other vegetables)**
  * Confidence: `0.136` (13.6%)
  * Lift: `1.11` → Weak but logical link (meat + veggies).

* **(yogurt) → (sausage)**
  * Confidence: `0.066` (6.6%)
  * Lift: `1.10` → Small, not very strong.

## Business Insights:
* **Sausage + Beer**  
   * Customers who buy sausage are slightly more likely to also buy bottled beer.
   * Action: Promote them together as a weekend BBQ combo.
* **Frankfurters + Vegetables** 
   * Strong association between frankfurters and vegetables suggests a meal-prep use case.
   * Action: Bundle them as a ready-to-cook family meal pack.
* **Yogurt + Sausage OR citrus fruit + yogurt** 
   * Customers who purchase yogurt often also buy sausage OR citrus fruit.
   * Action: Supermarkets can offer them in combo packs or discount bundles (e.g., yogurt + sausage meal pack, citrus fruit + yogurt health combo).
* **Whole Milk + Yogurt** 
   * Both items appear consistently across transactions.
   * Action: Keep them in close proximity on shelves to encourage add-on purchases.
* **Rolls/Buns + Sausage** 
   * Common pairing suggests easy meal/snack combinations.
   * Action: Offer small discounts when purchased together.
* **Targeted Promotions**
   * If a customer has “pastry” in their shopping cart, they can be offered a targeted coupon for yogurt or sausage.
   * Personalized offers = higher sales conversion.
* **Inventory Management**
   * Frequent items like yogurt, sausage, whole milk have consistently high demand, and avoiding stock-outs is critical.
   * Store managers should maintain a higher inventory buffer for these products.
* **Customer Segmentation**
   * Some rules highlight healthy combos (citrus fruit + yogurt) while others show party combos (sausage + beer + soda).
   * This helps identify different customer groups (health-conscious vs. party buyers), allowing more tailored marketing campaigns.

## Outputs:  
- [**View frequent_itemsets_apriori.csv**](https://github.com/khushi9179/Codectechnologies-Intern-MarketBasketAnalysis/blob/main/frequent_itemsets_apriori.csv)
- [**View frequent_itemsets_fpgrowth.csv**](https://github.com/khushi9179/Codectechnologies-Intern-MarketBasketAnalysis/blob/main/frequent_itemsets_fpgrowth.csv)
- [**View association_rules.csv**](https://github.com/khushi9179/Codectechnologies-Intern-MarketBasketAnalysis/blob/main/association_rules.csv) 

## Visualization's:
1.


## Conclusion:
Market Basket Analysis of the Groceries dataset revealed strong associations between items like **yogurt & citrus fruit, sausage & beer, frankfurter & vegetables**. These patterns can be used for **product bundling, cross-selling strategies, shelf placement, targeted promotions, and inventory planning**. By applying these insights, retailers can improve customer experience and increase overall sales.

This project demonstrates how Market Basket Analysis helps retailers to understand customer buying behavior. By applying Apriori algorithm and association rules, businesses can design better promotions, improve store layout, and increase cross-selling opportunities.
