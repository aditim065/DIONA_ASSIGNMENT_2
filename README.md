# Criminal Risk Assessment Request – XLSForm

This project converts the provided Criminal Risk Assessment Request PDF into an ODK-compatible XLSForm.

## Project files

- `source/Criminal Risk Assessment Request.pdf`
- `source/Sample XLS Form Reference.xlsx`
- `xlsform/Criminal_Risk_Assessment.xlsx` - New xlsform which is required for the assignment

## Implementation highlights

- Complete consent/release wording is preserved.
- The consent date is captured as a date field.
- The assessed person's signature is captured as an image/signature field.
- Unconsented is represented as Yes/No without interpreting an unchecked value as consent.
- Page 1 fields 1–10 are included.
- Gender is limited to MALE and FEMALE.
- Identification documents are represented using `select_multiple`.
- A minimum of two identification types is enforced; additional selections are allowed.
- Other (specify ID) appears when Other is selected and is required when displayed.
- The Manitoba driver's licence number appears when the Manitoba driver's licence option is selected and is required when displayed.
- The page 2 assessed-person name is calculated from page 1.
- Required page 2 fields are enforced.
- The last criminal risk assessment date and designate fax remain optional.
- Source explanatory and warning text is preserved.

The source requires TWO PIECES of identification. The digital form interprets that as a minimum of two selected identification types; additional identification types are allowed.

## Validation

The XLSForm was tested using XLSForm Online and returned "Form is valid!".

## Functional testing

The minimum-two-identification constraint and the conditional identification fields were tested.
