# BUG-007 - Active filter remains on hidden column and hides records

## Module

Contacts

## Severity

Medium

## Priority

Medium

## Environment

- Defalto CRM
- Contacts module
- Contact list view

## Preconditions

- Contact list contains multiple records.
- User has access to column management.
- A filter can be applied to a column.

## Steps to Reproduce

1. Open the **Contacts** module.
2. Apply a filter on a visible column (for example, filter **Last Name** by a value that does not exist).
3. Confirm that the list displays no records.
4. Open column management.
5. Hide the column used for filtering.
6. Observe the contact list.

## Actual Result

The filter applied to the hidden column remains active after the column is removed from the visible list.

The user cannot see which filter is affecting the results because the filtered column is no longer displayed.

The record list remains empty even though no visible filters are shown.

Restoring the hidden column displays the previously applied filter value again.

After logging out and logging back in:
- the filter is cleared,
- the hidden column remains hidden.

## Expected Result

When a column containing an active filter is hidden, the application should handle the existing filter state in a clear and predictable way.

Possible expected behaviours:
- remove the filter automatically,
- inform the user that an active filter exists on the hidden column,
- or provide a visible way to manage and clear active filters.

The user should not be left with an empty record list without any visible explanation.

## Business Impact

Users may incorrectly assume that records do not exist and attempt to create duplicate records.

For example, a user searching for an existing customer may not see the record because it is hidden by an invisible filter. The user may then try to create the same customer again and encounter duplicate validation errors without understanding the reason.

This can lead to user confusion, wasted time and reduced trust in the system.
