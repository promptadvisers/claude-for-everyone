---
name: receipt-checker
description: Create and check an Excel expense workbook from receipt PDFs or images. Use for receipt reconciliation, expense reports, or requests to use the Receipt checker skill.
---

# Receipt checker

Turn the receipts supplied for the current task into a traceable Excel workbook.

## Read the inputs

- Read each receipt and keep one row per source file, including separate receipts with identical totals.
- Record the source filename, vendor, receipt date, total amount, currency and any field needing review.
- Use the printed final total. Keep the receipt date distinct from a card settlement date.
- Use the currency printed on the receipt or the user's explicit currency instruction. A bare dollar sign does not establish USD. Mark an unresolved currency as unknown and flag it.
- Mark unreadable or ambiguous fields for review. Explain any assumptions briefly.

## Build the workbook

Create a new .xlsx file using the requested filename, or receipt_check.xlsx when none is given. Leave the original receipts alone.

Use two sheets.

1. Receipts has the columns Source file, Vendor, Date, Amount, Currency and Review notes. Store known amounts as numbers and use the same currency code consistently.
2. Summary lists each currency and calculates its total using live Excel formulas referencing the Receipts sheet. Include a formula for the source count and state how many rows need review. Keep different currencies in separate totals.

Do not replace formula cells with fixed answers or combine currencies without an explicit conversion instruction. If a source cannot be read, retain its row with a review note and exclude its unknown amount from the total.

## Check before returning

- Compare every workbook row with its receipt, including vendor, date, final amount and currency.
- Confirm that all supplied files are represented exactly once.
- Confirm the summary formulas include the full row range and keep currencies separate.
- Independently add the source totals within each currency and reconcile them to the workbook.
- Test a one-unit change in a disposable copy or in memory. Confirm the corresponding currency total changes by one, then retain the original amounts in the delivered workbook.

Return the workbook with the count of source files, each currency total and any unresolved fields. Tell the user which checks passed. If spreadsheet generation or formula recalculation is unavailable, state that limitation and provide the extracted rows and intended formulas for review.
