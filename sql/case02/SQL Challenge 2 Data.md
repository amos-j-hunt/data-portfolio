# SQL Challenge 2 Data & Methodology Overview
## Data Dictionary
### Table 1: runners
The ```runners``` table shows the ```registration_date``` for each new ```runner_id```
Customer pizza orders are captured in the customer_orders table with 1 row for each individual pizza that is part of the order.
### Table 2: customer_orders
The ```pizza_id``` relates to the type of pizza which was ordered whilst the ```exclusions``` are the ```ingredient_id``` values which should be removed from the pizza and the ```extras``` are the ```ingredient_id``` values which need to be added to the pizza.

Note that customers can order multiple pizzas in a single order with varying ```exclusions``` and ```extras``` values even if the pizza is the same type!
### Table 3: runner_orders
After each order is received through the system, it is assigned to a runner. However, not all orders are fully completed and can be cancelled by the restaurant or the customer.

The ```pickup_time``` is the timestamp at which the runner arrives at the Pizza Runner headquarters to pick up the freshly cooked pizzas. The ```distance``` and ```duration``` fields are related to how far and long the runner had to travel to deliver the order to the respective customer.
### Table 4: pizza_names
At the moment - Pizza Runner only has 2 pizza types (```pizza_name```) available: the Meat Lover's and Vegetarian!
### Table 5: pizza_recipes

Each ```pizza_id``` has a standard set of ```toppings``` which are used as part of the pizza recipe.
### Table 6: pizza_toppings

This table contains all of the ```topping_name``` values with their corresponding ```topping_id``` value.
## Methodology
PostgreSQL v13 was used for data cleaning and analysis.

The ```exclusions``` and ```extras``` columns in the ```customer_orders``` table and the ```cancellation``` column in ```runner_orders``` had some inconsistencies. There were missing values, ```null``` values, and ```nAn``` values. I have normalized these as all ```null``` values.

The ```distance``` and ```duration``` columns had inconsistent formatting. Unnecessary text was removed, and non-standard empty values were normalized to ````null````.

Furthermore, the ```customer_orders``` table did not have a unique identifier, so I added ```order_line_id``` as a surrogate foreign key to facilitate analysis.

I have written a SQL query for each of the questions posed by Pizza Runner about their data. Results can be improved with clarified requirements. Lacking this information, I have made and recorded several assumptions about what information is actually desired.