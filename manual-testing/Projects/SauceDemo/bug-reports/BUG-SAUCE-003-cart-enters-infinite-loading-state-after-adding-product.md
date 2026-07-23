# Bug Report

## Title
Cart enters infinite loading state after adding a product

## Environment
SauceDemo web application

## Severity
High

## Priority
High

## Description
After adding a product to the cart from the product details page, opening the cart causes the application to enter an infinite loading state. The loading spinner remains visible indefinitely, preventing the user from accessing the cart.

## Steps to Reproduce
1. Log in to the application.
2. Open any product details page.
3. Click **Add to cart**.
4. Wait for the add-to-cart animation to complete.
5. Click **My Cart**.

## Expected Result
The cart should open immediately and display the added product.

## Actual Result
The cart does not load. An infinite loading spinner is displayed and the cart content is never shown.

## Additional Information
- The issue was reproduced with multiple products.
- The product is successfully added to the cart.
- The cart counter is updated correctly.
- Clicking the cart button again closes the cart panel, but opening it again results in the same infinite loading state.
- Refreshing the page (F5) restores normal operation and the previously added product is visible in the cart.
- Adding another product after refreshing reproduces the issue again.
