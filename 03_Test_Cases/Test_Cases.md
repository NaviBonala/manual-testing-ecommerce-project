## Login
| Test Case ID | Test Scenario ID | Test Case Description | Preconditions | Test Steps | Test Data | Expected Result |
|-------------|------------------|----------------------|---------------|------------|-----------|-----------------|
| TC_01 | TS_01 | Verify login with valid credentials | User is on the SauceDemo login page | 1. Enter valid username<br>2. Enter valid password<br>3. Click Login | Username: standard_user<br>Password: secret_sauce | User is logged in and redirected to products page |
| TC_02 | TS_02 | Verify login fails with invalid username | User is on the SauceDemo login page | 1. Enter invalid username<br>2. Enter valid password<br>3. Click Login | Username: abcde<br>Password: secret_sauce | Error message displayed |
| TC_03 | TS_03 | Verify login fails with invalid password | User is on the SauceDemo login page | 1. Enter valid username<br>2. Enter invalid password<br>3. Click Login | Username: standard_user<br>Password: sauce | Error message displayed |
| TC_04 | TS_04 | Verify login fails with empty fields | User is on the SauceDemo login page | 1. Leave username empty<br>2. Leave password empty<br>3. Click Login | Username: blank<br>Password: blank | Error message displayed |
| TC_05 | TS_05 | Verify login fails for locked-out user | User is on the SauceDemo login page | 1. Enter locked-out username<br>2. Enter valid password<br>3. Click Login | Username: locked_out_user<br>Password: secret_sauce | Locked-out error message displayed |


## Cart
| Test Case ID | Test Scenario ID | Test Case Description | Preconditions | Test Steps | Expected Result |
|-------------|------------------|----------------------|---------------|------------|-----------------|
| TC_06 | TS_11 | Verify adding single product to cart | User is logged in and is on the products page. | 1. Click the "Add to cart" button<br>2. Navigate to the shopping cart page | The correct product is added to the cart, the cart icon updates to (1), and the product details are accurate |
| TC_07 | TS_12 | Verify adding multiple items to cart | User is logged in and is on the products page. | 1. Click the "Add to cart" button on the product A.<br>2. Navigate to product B<br>3. Add the product B to the cart<br>4. Navigate to the cart page | Both products appear as separate line items |
| TC_08 | TS_13 | Verify removing the product from cart | User is logged in and is on the products page. | 1. Click the "Add to cart" button on the product.<br>2. Navigate to cart page<br>3. Click "Remove" button of the product. | Products removed from the cart |
| TC_09 | TS_14 | Verify cart badge updates correctly | User is logged in and is on the products page. | 1. Click the "Add to cart" button on the product.<br>2. Navigate to cart page | Cart badge increments according to the number of products added | 
| TC_10 | TS_15 | Verify cart retains items after page refresh | User logged into the application and is on the products page | 1. Click the "Add to cart" button on the product.<br>2. Refresh the page | Cart contents persist after refresh |

## Checkout 
| Test Case ID | Test Scenario ID | Test Case Description | Preconditions | Test Steps | Expected Result |
|-------------|------------------|----------------------|---------------|------------|-----------------|
| TC_11 | TS_16 | Verify user can proceed to checkout from cart | User is logged in, has items in the cart, and is on the cart page. | 1. Click on the "Checkout" button. | User is navigated to the checkout information page. |
| TC_12 | TS_17 | Verify checkout fails when mandatory fields are empty | User is logged in, has items in the cart, and is on the cart page | 1. Click on the "Checkout" button.<br>2. Leave the mandatory fields blank.<br>3. Click "Continue" | Error message should be displayed for the mandatory fields |
| TC_13 | TS_18 | Verify successful checkout with valid user details | User is logged in, has items in the cart, and is on the cart page | 1. Click on the "Checkout" button.<br>2. Enter the mandatory fields.<br>3. Click "Continue".<br>4. Click "Finish" | Order confirmation page is displayed. | 
| TC_14 | TS_19 | Verify checkout fails for invalid postal code | User is logged in, has items in the cart, and is on the cart page | 1. Click on the "Checkout" button.<br>2. Enter an invalid postal code.<br>3. Click "Continue" | Error message displayed and user remains on checkout information page. | 
| TC_15 | TS_21 | Verify order confirmation message is displayed after successful checkout | User is logged in, has items in the cart, and is on the cart page |  1. Click on the "Checkout" button.<br>2. Enter mandatory fields.<br>3. Click "Continue"<br>4. Click "Finish" | Order confirmation message is displayed successfully. |
