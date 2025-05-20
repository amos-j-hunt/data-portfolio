# SQL Challenge 1 Data & Methodology Overview
## Data Dictionary
### Table 1: sales
The sales table captures all customer_id level purchases with a corresponding order_date and product_id information for when and what menu items were ordered.
### Table 2: menu
The menu table maps the product_id to the actual product_name and price of each menu item.
### Table 3: members
The final members table captures the join_date when a customer_id joined the beta version of the Danny’s Diner loyalty program.
## Methodology
I have written a SQL query for each of the questions posed by Danny’s Diner about their data. Since it was requested that the results would be accessible on demand, I have structured them as views that can be accessed with very simple queries.
Results can be improved with clarified requirements, information about the membership onboarding flow, and a more complete time-stamp. Lacking this information, I have made and recorded several assumptions about what information is actually desired.

