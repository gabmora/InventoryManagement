# DAMLize Inventory ✅
DAML Fundemental Capstone - Inventory Management system 

I. Overview 
Created a new project in "InventoryManagement" based on the template "skeleton".
DAMLize Inventory is an inventory management system.
Suppliers can create products to add to inventory. Suppliers can update stock and prices of products. Customers can place orders based on products (customers are observers of product contracts) and suppliers can accept orders, therefore automatically updating quantity. Customers also have the choice of canceling their orders.

II. Workflow
Supplier creates a Product contract
  optional: supplier exercises UpdateStock to update quanity of inventory for a specific product
  optional: supplier exercises UpdatePrice change price of product 
customer creates Order contract based on products avalible by supplier, entering orderId meaningful to customer, productId, and quantity. 
supplier exercises AcceptOrder on Order contract OR customer exercises CancelOrder on Order contract

III. Challenges 
daml start open navigator but does not show contracts from test scripts Solution: removed parties from .yaml and created users in Setup. I also had two setup scripts(one in setup and one in test, changed the test sestup name to avoid confusion)
CancelOrder choice was not consuming the Order contract properly. Solution: made it a nonconsuming choice that returns nothing and archives self.
Attempted to create realistic supply chain model with both manufacter and suppliers where manufactuers create products and suppliers distributes but was too complex so I simplified the templates to only have suppliers and customers.

IV. Complining & Testing
To compile and test, run the pre-written script in the Setup.daml under /daml OR run:

$ daml start
