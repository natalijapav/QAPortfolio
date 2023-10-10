***Test Case 1 : Decision Table***

  **Conditions**   **All fields are properly filled**   **All fields are left empty**   **Some fields are left empty, some are not, randomly**   **Some fields are filled, some are left empty, randomly**
  ---------------- ------------------------------------ ------------------------------- -------------------------------------------------------- -----------------------------------------------------------
  First Name       FILL                                 Empty                           Empty                                                    Fill
  Last Name        Fill                                 Empty                           Empty                                                    Fill
  Country          \*                                   \*                              \*                                                       \*
  Street Address   Fill                                 Empty                           Empty                                                    Fill
  Town             Fill                                 Empty                           Fill                                                     Empty
  Postcode         Fill                                 Empty                           Fill                                                     Empty
  Phone            Fill                                 Empty                           Fill                                                     Empty
  Email            Fill                                 Empty                           Fill                                                     Empty
  **OUTPUT**       Pass                                 Fail                            Fail                                                     Fail

Test Case Name: Verify user can submit order with all required fields.

Description: Verify if user can place order with filing all the
mandatory field in billing details.

Preconditions: Add one product in the cart.

+--------------------+--------------------+--------------------+--------------------+
| **Test Steps**     |                    | **Test Data**      | **Expected         |
|                    |                    |                    | result**           |
+====================+====================+====================+====================+
| 1.Go to Katalon    |                    | https://cms.demo.k | User is redirected |
| shop               |                    | atalon.com/cart/   | to the Cart page   |
|                    |                    |                    |                    |
| cart               |                    |                    |                    |
+--------------------+--------------------+--------------------+--------------------+
| 2.Scroll down to   |                    |                    | Checkout page is   |
| Cart totals and    |                    |                    | opened             |
| click Proceed to   |                    |                    |                    |
| Check out          |                    |                    |                    |
+--------------------+--------------------+--------------------+--------------------+
| 3.Fill all the     |                    | Name: Nat          | Provided value are |
| fields in Billing  |                    |                    | displayed in the   |
| details with given |                    | Last name: Pavl    | fields             |
| test data          |                    |                    |                    |
|                    |                    | Street address: xy |                    |
|                    |                    | 23                 |                    |
|                    |                    |                    |                    |
|                    |                    | Town: tamo         |                    |
|                    |                    |                    |                    |
|                    |                    | Postcode: 1234     |                    |
|                    |                    |                    |                    |
|                    |                    | Phone:123456789\   |                    |
|                    |                    | Email:nana@nana.co |                    |
|                    |                    | m                  |                    |
+--------------------+--------------------+--------------------+--------------------+
| 4\. Click on dropd |                    | Serbia             | Provided value is  |
| own menu for choos |                    |                    | selected           |
| ing ‘Country’      |                    |                    |                    |
+--------------------+--------------------+--------------------+--------------------+
| 5.Click on Place   |                    |                    | Order received     |
| order              |                    |                    | page is opened and |
|                    |                    |                    |                    |
|                    |                    |                    | message ‘’Thank    |
|                    |                    |                    | you. Your order    |
|                    |                    |                    | has been           |
|                    |                    |                    | received.’’ is     |
|                    |                    |                    | shown with order   |
|                    |                    |                    | details            |
+--------------------+--------------------+--------------------+--------------------+

**Test Case 2: Boundary value analysis**

  Test Data using BVA method
  ----------------------------
  0

Test Case Title: Verify products in cart can be updated if value is zero

Description: Verify product can be updated using zero value and with
zero value product is removed from the cart.

  **Test Steps**                                            **Test Data**                  **Expected Results**
  --------------------------------------------------------- ------------------------------ -----------------------------------------------------------------------------------------------------------
  1.Go to Katalon Shop                                      https://cms.demo.katalon.com   User is redirected to Katalon shop page
  2.Scroll down to Shop                                                                    Products are displayed
  3.Hover over product Flying Ninja and click Add to cart                                  View cart is shown on upper right corner
  4.Click on View cart on upper right corner                                               Cart page is opened, product is shown in cart, quantity is 1
  5.In Quantity field enter data                            0                              Text message is displayed ‘’Cart updated.’’ ‘’Your cart is currently empty.’’ is displayed. Quantity is 0

**Test Case 3: Error Guessing**

Test Case Title: Verify sorting products by low/high prices

Description: Verify if the products are sorted by prices, low to high
and high to low

  **Test Steps**                                             **Test Data**                  **Expected results**
  ---------------------------------------------------------- ------------------------------ ----------------------------------------------------------------------------------------------------
  1.Go to Katalon shop                                       https://cms.demo.katalon.com   User is redirected to Katalon shop page
  2.Click on Default sorting dropdown list on the right                                     Dropdown list is opened
  3.Click on Sort by price: Low to high from dropdown list                                  ‘Sort by price: Low to high’ is shown in dropdown menu, and products are sorted by low-high prices
  4\. Click on the Dropdown menu                                                            Dropdown list is opened
  4.Click on Sort by price: High to low from dropdown list                                  Products are sorted by high-low prices

**Test Case 4: Error guessing**

Test Case Title: Verify search can find the existing value from the page

Description: Verify search box is filtering products with specified
data. Search box is on the left, in ‘’Type to search’’ field enter
specific title of the product

  **Test Steps**                                                       **Test Data **                 **Expected results**
  -------------------------------------------------------------------- ------------------------------ -------------------------------------------------------------------------------
  1.Go to Katalon shop                                                 https://cms.demo.katalon.com   User is redirected to Katalon shop page
  2.In search text fields enter existing value, example in Test Data   ‘’Ninja’’                      Products with ‘’Ninja’’ in title are listed on page Search Results for: Ninja
                                                                                                      

**Test Case 5: Error guessing**

Test Case Title:Verify user can undo action on Cart page.

Description:Verify Undo option on cart page working when item is removed
from cart and product is back in cart

  **Test Steps**                                            **Precondition**               **Test Data **                 **Expected results**
  --------------------------------------------------------- ------------------------------ ------------------------------ --------------------------------------------------------
                                                            1.Have 1 product in the cart                                  
  2.Go to Katalon shop page, scroll down to Shop                                           https://cms.demo.katalon.com   User is redirected to the page, products are displayed
  3.Hover over product Flying Ninja and click Add to cart                                                                 View cart is shown on upper right corner
  4.Hover over product Happy Ninja and click Add to cart                                                                  View cart is shown on upper right corner
  5.Click on View cart on upper right corner                                                                              Cart page is opened, product is shown in cart
  6.Click on red X to remove item from the cart                                            Happy Ninja                    ‘’‘’Happy Ninja’’ removed.Undo?’’ message is dispayed
  7.Click on ‘’Undo?’’                                                                                                    Happy Ninja item is back in cart
