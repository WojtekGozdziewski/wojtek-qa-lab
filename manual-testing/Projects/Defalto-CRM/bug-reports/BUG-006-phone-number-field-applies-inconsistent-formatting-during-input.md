# BUG-006 - Phone number field applies inconsistent formatting during input

## Module

Contacts

## Severity

Medium

## Priority

Medium

## Environment

- Defalto CRM
- Contacts module
- Add/Edit Contact form

## Preconditions

User is creating or editing a contact.

## Steps to Reproduce

1. Open the **Contacts** module.
2. Create a new contact or edit an existing one.
3. In the **Primary Phone** field, manually enter repeated digits (e.g. 2222, 3333, 4444, 666666666).
4. Observe the formatting applied while typing.
5. Repeat the test by pasting the same values into the field.
6. Save the record.

## Actual Result

The phone number field applies inconsistent automatic formatting depending on the entered digit sequence.

Examples observed during testing:

| Entered value | Displayed value |
|---------------|-----------------|
| 111           | 111 |
| 222           | 2/22 |
| 2222          | 2/222 |
| 333           | 33/3 |
| 444           | 44/4 |
| 555           | 55/5 |
| 666666666     | 666 666 666 |
| 777           | 777 |
| 888888888     | 888 888 888 |
| 999999999     | 999 999 999 |

Additional observations:

- Manual typing and pasting produce different behaviour while editing.
- After pasting, the value initially appears unformatted.
- Once the field loses focus or the record is saved, the application applies the same inconsistent formatting.
- Automatically inserted formatting characters become part of the stored phone number.
- Records containing these automatically formatted values can be saved successfully.
- After entering a tenth digit, all automatic formatting disappears and the value becomes a continuous sequence of digits.

## Expected Result

The phone number field should apply one consistent formatting rule regardless of the entered digits or input method.

The application should not automatically insert unexpected formatting characters into the phone number value.

Formatting should be consistent during typing, pasting and saving.

## Business Impact

Phone numbers are stored in inconsistent formats depending on the entered digit sequence and input method. This may lead to incorrect data presentation, reduced data quality and decreased user confidence in the application's input validation.
