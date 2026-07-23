# Bug Report

## Title
Checkout allows invalid character-only input in multiple required address fields

## Environment
SauceDemo web application

## Severity
Medium

## Priority
Medium

## Description
The checkout form accepts values consisting entirely of special characters in several required shipping address fields. The entered values pass validation and the checkout process continues to the payment step.

## Steps to Reproduce
1. Add any product to the cart.
2. Proceed to Checkout.
3. Fill the required shipping fields with the following values:
   - Last Name: `********`
   - Address: `*******`
   - Postal Code: `01-100`
   - City: `&&&&&`
4. Complete the required payment fields with any test values.
5. Click **Pay Now**.

## Expected Result
Required address fields should reject values consisting only of special characters and prompt the user to enter valid address information before continuing.

## Actual Result
The shipping address is accepted without validation errors. The checkout process proceeds to the payment verification step, where the only reported issue is payment verification. No validation errors are displayed for the invalid shipping address fields.

## Additional Information
- The issue affects multiple required fields:
  - Last Name
  - Address
  - City
- Postal Code is validated separately and accepts correctly formatted postal codes.
- Selecting **"Use shipping address as billing address"** copies the invalid shipping data to the billing address as well, propagating invalid customer information further in the checkout process.
