# Illustrative document journeys

The examples below use invented names, dates, and amounts. They show the decisions a reviewer can expect without reproducing a real invoice, payment receipt, or production log.

## Purchase invoice: ready to record

An uploaded purchase invoice is readable and contains a supplier, invoice number, date, line items, tax, and total. The workflow extracts those fields, validates the buyer and accounting data, checks for an existing invoice, and resolves the supplier and expense account. When the checks pass, it records the invoice in Daftra, attaches the original file, and updates the status visible to the uploader.

**Outcome:** recorded, with a link to the ERP record in the private activity log.

## Purchase invoice: review required

An otherwise readable invoice contains a supplier name that cannot be matched confidently to the supplier account. The workflow preserves the document and its extracted fields, stops before posting, and records why it needs attention.

**Outcome:** manual review, with a specific reason and no automatic invoice creation.

## Supplier payment: unclear beneficiary

A bank receipt shows an amount and date but does not establish which supplier account should receive the payment. The operator selects the supplier and payment account. After posting, the workflow reads the saved payment to confirm the result. If confirmation is unavailable, the status remains for reconciliation rather than starting another financial POST automatically.

**Outcome:** waiting for selection, confirmed payment, or manual reconciliation depending on the evidence available.

These paths illustrate behavior, not a claim that every document format or accounting exception can be processed automatically.
