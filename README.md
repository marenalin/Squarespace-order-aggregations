# Squarespace-order-aggregations
Generate and email sorted packing lists and daily inventory from the SquareSpace Orders API using an automated Google Script

This code references and updates a Google Sheets file with a tab that has the full list of items in inventory and for sale on the online squarespace site. 

Set the name of the spreadsheet to be updated with imported orders:
var SHEET_NAME = "Squarespace_Imported_Orders"; 

Set the name of the inventory sheet:
var MASTER_SHEET_NAME = "Master (Reformatted)"; //key with all the product SKUs and categories are

Set the email address that will receive these packing lists and inventory aggregations:
var WHOM_TO_EMAIL = "orders@somerestaurant.com"; //which email address are you sending the packing list to?

The columns of the master SKUs sheet are ordered as the following:
[A] ITEM 
[B] NAME	
[C] CATEGORY	
[D] SKU	

The SKUs match those in the Squarespace account.

The sheet that is updated to log all squarespace orders (by line item) has the following columns:
[A] full json for the item line
[B] Name of client
[C] Name of the sales item
[D] Blank
[E] Date of the order
[F] Name of variation ordered (e.g. size/color)
[G] Quantity ordered
[H] Price of each item
[I] Phone number
[J] Email

