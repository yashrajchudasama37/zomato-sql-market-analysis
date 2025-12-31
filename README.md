# EXECUTIVE SUMMARY:
* Zomato Hyderabad: A Dive into Hyperlocal Food-Tech
* Data Source: Kaggle | Scale: 1,231 Menu Items & Restaurant Records

#The Zomato Context
Most of us recognize Zomato as India's multinational restaurant aggregator and food delivery giant. The motivation behind analyzing this specific dataset is to peek "under the hood" of their operations in a high-growth market like Hyderabad. While global datasets give us a broad view,
this 1,231-row segment allows us to see exactly how individual neighborhoods function—from the competitive pricing of Biryani to the premium charged for "Bestseller" items. 

# Exploring the Data with SQL
While exploring the 1,231 rows of data, I focused on building a clean and reliable foundation for my analysis:
* Schema Audit: I began by checking column names, data types, and constraints to ensure the database schema was optimized for 1,231 records.
* Integrity Validation: Validated the completeness of ratings and identified price outliers to ensure the data was not skewed by extreme values.
* Handling Nulls: I applied the (COALESCE) function to transform missing (best_seller) values into 'Regular' status, ensuring no menu item was left unmanaged during analysis.
* Data Deduplication: To ensure accuracy, I removed duplicate menu items by retaining only those records with the highest customer engagement (votes).
* Operational Control: Managed SQL safe mode to allow for precise data cleanup and deletion without compromising the core dataset. 

# Analyzing the Data: Key Strategic Insights:
After cleaning and exploring the dataset, I derived several insights that explain the "Price Persona" of the Hyderabad food market:
* The Locality Advantage: I discovered that neighborhood-level analysis (place_name) is far more valuable than city-level data, as it revealed specific demand patterns unique to different parts of Hyderabad.
* Cuisine Supply Gaps: By mapping food supply by neighborhood, I identified specific localities where certain cuisines are underserved, providing a roadmap for potential restaurant expansion.
* The "Star" Item Premium: My analysis confirmed that items marked as BESTSELLER or MUST TRY are generally priced higher than regular items, proving that customers are willing to pay for perceived excellence.
* Market Segmentation: I built a price-category model where I found that most items fall into the 'Medium' (200–500) bracket, identifying this as the "mass-market sweet spot" for Hyderabad.
* Engagement Efficiency: Surprisingly, I found that larger menus do not always drive more engagement; restaurants with focused, high-performing menus often outperformed those with massive variety.

# Project Conclusion
* This project demonstrates the ability to transform 1,231 raw data points into a strategic market audit. By using advanced SQL techniques like Window Functions and Conditional Aggregation, I was able to validate pricing strategies and identify market leaders. Ultimately, this analysis proves that in the food-tech business, understanding hyperlocal trends and quality-based pricing is the key to capturing the customer's plate.


