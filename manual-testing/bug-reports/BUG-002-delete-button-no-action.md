# BUG-002: Delete button does not perform any action

## Application

Defalto CRM (Cloud Trial)

## Module

Contractors / Contacts / Potential Customers

## Severity

Medium

## Priority

Medium

## Summary

The delete button is visible in the record preview view, but clicking it does not trigger any action.

The user interface suggests that record deletion is available, but the functionality is not working.

## Preconditions

- User is logged in.
- Existing contractor, contact or potential customer record is available.

## Steps to reproduce

1. Open any existing record.
2. Navigate to the record preview/details view.
3. Locate the delete button in the top-right corner.
4. Click the delete button.

## Actual result

Clicking the delete button does not perform any action.

No confirmation dialog, notification or error message is displayed.

## Expected result

The system should either:

- allow the user to delete the record after confirmation,
or
- hide/remove the delete button if deletion is not available from this view.

## Business impact

A non-functional action button may confuse users and reduce confidence in the system.

Users may be unsure whether the action was completed or whether the system is working correctly.

## Test result

Failed
