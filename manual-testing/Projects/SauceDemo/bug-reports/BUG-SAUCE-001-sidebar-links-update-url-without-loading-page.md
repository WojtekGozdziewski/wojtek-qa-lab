# Bug Report

## Title
Sidebar navigation links update URL but do not load corresponding page

## Environment
SauceDemo web application

## Severity
Medium

## Priority
Medium

## Description
The "Wishlist" and "Refer a friend" links in the left sidebar navigation do not open their corresponding pages. The links appear to be active and clickable, and the browser URL changes after clicking, but the application content remains unchanged.

## Steps to Reproduce
1. Log in to the application.
2. Open the left sidebar menu.
3. Click on the "Wishlist" link.
4. Observe the URL change.
5. Refresh the page.
6. Repeat the same steps for the "Refer a friend" link.

## Expected Result
Clicking an active navigation link should open the corresponding page or display appropriate information.

## Actual Result
The URL changes to:
- `sauce-show-wish-list`
- `sauce-show-refer-a-friend`

However, the displayed content remains the product list page. Refreshing the page does not load the expected view.

## Additional Information
Other sidebar navigation links were tested and work correctly:
- Home
- Catalog
- All Items
- About
- Blog
- Logout

The issue appears to be limited to the "Wishlist" and "Refer a friend" navigation items.
