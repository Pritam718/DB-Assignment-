
# DB-Assignment Answer

### 1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.

The relationship between "Product" and "Product_Category" is a one-to-many relationship. Here's what this means:

One Product: A single product can belong to only one category. For example, a t-shirt can be categorized as "Clothing" but not "Electronics" simultaneously.
Many Products: A single category can have many products associated with it. For instance, the "Clothing" category might contain t-shirts, pants, dresses, and more.


### 2. How could you ensure that each product in the "Product" table has a valid category assigned to it?


There are two primary methods to guarantee that every product in the "Product" table has a valid category assigned:

### 1. Foreign Key Constraint:

Establish a foreign key constraint on the category_id column in the "Product" table.
This foreign key references the primary key (id) of the "Product_Category" table.
By doing this, it's enforced that any value entered into the category_id column must exist as a legitimate category ID in the "Product_Category" table.


### 2. Data Validation:

During application development, incorporate data validation logic to verify that the selected category ID for a product actually exists within the "Product_Category" table before adding or updating the product data.
This two-pronged approach provides a robust mechanism for ensuring valid category assignment and data integrity.
