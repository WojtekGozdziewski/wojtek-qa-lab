# UX Improvement Report

## Title
Missing quantity adjustment option in cart view

## Application
SauceDemo web application

## Category
Usability / User Experience

## Description
The cart view does not provide an option to modify the quantity of products already added to the cart.

Users can remove a product from the cart, but they cannot directly increase or decrease the quantity from the cart page.

## Steps to Reproduce
1. Add the same product multiple times to the cart (e.g. Grey Jacket).
2. Open the cart view.
3. Try to change the product quantity.

## Current Behavior
- The cart displays the product quantity.
- There are no controls for increasing or decreasing the quantity.
- Removing the product removes the item completely from the cart.
- To modify the quantity, the user needs to continue to another checkout step and update the quantity there.

## Expected Behavior
The cart view should provide a simple way to adjust product quantity, for example:
- editable quantity field,
- plus/minus buttons,
- quantity update controls.

## User Impact
Users may have difficulty correcting their order before checkout.

For example, a customer who accidentally adds two items instead of one must leave the cart view and navigate further into the checkout process to make a simple quantity correction.

## Recommendation
Add quantity adjustment controls directly in the cart view to allow users to manage their order before proceeding to checkout.
