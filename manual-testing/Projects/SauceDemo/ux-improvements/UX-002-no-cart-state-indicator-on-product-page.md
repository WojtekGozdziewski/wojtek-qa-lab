# UX Improvement Report

## Title
No cart state indicator on product pages after adding a product

## Application
SauceDemo web application

## Category
Usability / User Experience

## Description
After adding a product to the cart, the product page does not provide any visual indication that the product is already present in the cart.

The Add to cart button remains unchanged and the user cannot determine from the product page whether the item was already added.

## Steps to Reproduce
1. Open any product details page.
2. Click **Add to cart**.
3. Return to the same product page.

## Current Behavior
- The button still displays **Add to cart**.
- No information indicates that the product is already in the cart.
- The user must open the cart view to verify the current cart contents.

## Expected Improvement
Provide a visual indication that the product has already been added, for example:
- change button state,
- display "Added to cart" information,
- show current quantity.

## User Impact
Users may be uncertain whether their action was completed and may accidentally add additional quantities of the same product.
