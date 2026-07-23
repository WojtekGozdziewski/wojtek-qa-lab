# Bug Report

## Title
Product search returns unrelated products for unmatched search queries

## Environment
SauceDemo web application

## Severity
Medium

## Priority
Medium

## Description
The product search function returns unrelated products when searching for terms that do not exist in the product catalog. The application displays the message "Showing results for [search term]" even though the displayed products do not match the entered search criteria.

## Steps to Reproduce
1. Log in to the application.
2. Navigate to the product list.
3. Enter a random search phrase that does not exist in the product catalog (for example: "xxxxx").
4. Submit the search.
5. Observe the displayed results.

## Expected Result
If no products match the entered search phrase, the application should display an empty result message or indicate that no products were found.

## Actual Result
The application displays:
"Showing results for xxxxx"

However, unrelated products are displayed:
- Black Heels
- White Sandals

The returned products are valid product pages and can be opened normally, but they do not match the search criteria.

## Additional Information
Additional searches were performed:
- "yyyyy"

The application returned unrelated products instead of displaying no matching results.

For existing search terms (for example "jacket"), matching products are displayed, but unrelated products may also appear.
