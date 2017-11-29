---
title: Backorders
taxonomy:
    category: docs
---

How to make product "backorderable":

1. Log in to NetSuite.
2. Navigate to the `List > Website > Items` https://www.screencast.com/t/c0igGS9QH
![](https://wiki.rocketweb.com/download/attachments/23954309/2017-03-06_1535.png)
3. Find the product and click "Edit" button. 
4. Check "Backorderable" checkbox in Classification section and save the product:
![](https://wiki.rocketweb.com/download/attachments/23954309/2017-03-06_1537.png)
5. Wait for 10-15 minutes until changes are imported to Magento.
6. Log in to Magento Admin.
7. Navigate to `Products > Catalog`
8. Find the product and open product details page.
9. Make sure that "Backorderable" setting is set to "Yes" :
![](https://wiki.rocketweb.com/download/attachments/23954309/2017-03-06_1606.png)

[notice]
Stocks:
1. Backorder product can have stock, in which case it is not a backorder. That attribute controls whether the product is backorderable, not necessary that it is a backorder at that moment. 
2. When importing stocks, check for the quantity reported by NetSuite: if the quantity is zero and product is backorderable, then stock is infinite. So Magento can treat backorders as "in stock products".

**PayPal restriction:**
*PayPal payment method is not available if product is backorderable and has no stock in NetSuite*
[/notice]
 
