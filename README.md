# DAMLize Inventory ✅
DAML Fundemental Capstone - Inventory Management system 

I. Overview 
Created a new project in "InventoryManagement" based on the template "skeleton".
DAMLize Inventory is an inventory management system.
Manufactuers can create products to add to inventory. Manufactuers can update stock and prices of products. Customers can place orders based on products and manfactuers can accept orders, therefore automatically updating quantity. Customers also have the choice of canceling their orders.

II. Workflow
manufactuer creates a Product contract
optional: manufactuer exercises UpdateStock to update quanity of inventory for a specific product
optional: manufactuer exercises UpdatePrice change price of product 
customer creates Order contract based on products avalible by manufactuer
manufactuer exercises AcceptOrder on Order contract OR customer exercises CancelOrder on Order contract

III. Challenges 
daml start open navigator but does not show contracts from test scripts 
CancelOrder choice was not consuming the Order contract properly. Solution: made it a nonconsuming choice that returns nothing and archives self.

IV. Complining & Testing
To compile and test, run the pre-written script in the Test.daml under /daml OR run:

$ daml start
