# Exploratory Testing Report: CRM Data Relationships and Dependencies

## Project
Defalto CRM

## Testing Area
Relationship handling between:
- Contractors
- Contacts
- Sales Opportunities

## Testing Approach
Exploratory testing focused on verifying consistency of relationships between CRM entities and checking how the system behaves during create, update and delete operations.

The goal was to identify potential data integrity issues and unexpected behavior from a user perspective.

## Tested Scenarios

### Sales Opportunity creation without customer association

The system allows creating Sales Opportunities without assigning:
- Contact
- Organization (Contractor)

This behavior may lead to creation of sales records without a clear business context.

Related issue:
- BUG-004: Sales Opportunity can be created without customer association

---

### Relationship between Contacts and Contractors

Observed behavior:
- Contacts can be linked to Contractors.
- The relationship is created from the Contact side.
- Contractor records do not display related Contacts in an easily accessible way.

This may reduce visibility of customer relationships for users managing Contractor records.

---

### Relationship between Sales Opportunities, Contacts and Contractors

Observed behavior:
- Sales Opportunities can be linked to Contacts.
- Sales Opportunities can be linked to Organizations (Contractors).
- The system allows these relationships to exist independently.

Additional testing showed that deleting one related entity may affect Sales Opportunities differently depending on which relationship is used.

---

## Delete Behavior Testing

Observed results:

| Action | Result |
|---|---|
| Delete Contractor linked to Sales Opportunity | Sales Opportunity is removed |
| Delete Contact linked to Sales Opportunity | Sales Opportunity remains |
| Delete Sales Opportunity linked to Contact and Contractor | Opportunity is removed without additional dependency warning |

Related issue:
- BUG-005: Inconsistent related record deletion behavior between CRM modules

---

## Findings

The tested modules contain multiple relationships between the same business entities. The current behavior may create uncertainty for users regarding:
- ownership of Sales Opportunities,
- impact of deleting related records,
- visibility of customer history.

The system would benefit from clearly defined relationship rules and consistent dependency handling.

## Business Risk

Potential risks:
- accidental loss of sales information,
- creation of unassigned Sales Opportunities,
- inconsistent customer data,
- reduced confidence in CRM records.

## Recommendation

Review the intended business model for relationships between:
- Contractors,
- Contacts,
- Sales Opportunities.

Ensure that:
- required relationships are enforced,
- deletion rules are consistent,
- users are informed about affected related records before destructive actions.
