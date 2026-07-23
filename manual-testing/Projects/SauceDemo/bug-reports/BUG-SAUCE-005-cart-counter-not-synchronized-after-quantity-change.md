# Bug Report

## Title
Cart counter is not synchronized with cart quantity after checkout flow

## Environment
SauceDemo web application

## Severity
Medium

## Priority
Medium

## Description
After changing the product quantity during the checkout flow, the cart counter displayed in the navigation bar is not immediately synchronized with the actual cart quantity.

The cart content and the cart counter show different values until the page is reloaded through navigation.

## Steps to Reproduce
1. Add one product (e.g. Grey Jacket) to the cart.
2. Open the cart.
3. Click **Checkout**.
4. On the checkout page, change the product quantity from `1` to `5`.
5. Click **Checkout** again.
6. On the payment/summary page, click the browser **Back** button.

## Expected Result
The cart counter in the navigation bar should display the same quantity as the cart content.

## Actual Result
After returning with the browser Back button:
- The product quantity displayed in the cart page is `5`.
- The cart counter in the navigation bar still shows `(1)`.

After clicking another navigation link (e.g. Home), the cart counter updates automatically and changes from `(1)` to `(5)`.

## Additional Information
The issue causes inconsistent information to be displayed to the user. Different parts of the application show different cart states until the page content is refreshed.
