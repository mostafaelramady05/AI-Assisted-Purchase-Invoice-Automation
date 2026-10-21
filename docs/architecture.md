# Architecture and implementation decisions

[Back to the project](../README.md)

This document organizes the behavior described in the project case study. It does not expose the private production configuration or claim independent execution verification.

## Accounting routing

The document type determines the next accounting path:

| Document | Path |
| --- | --- |
| Purchase invoice | Check invoice data, buyer, duplicates, and supplier before ERP posting. |
| Simplified tax invoice | Use the separate journal-entry path and check its attachment. |
| Supplier payment receipt | Resolve the supplier through human selection when it is not established by the document, then use the payment path. |

The distinction matters because extracting the same fields does not make these transactions interchangeable.

## Validation boundary

Extraction produces structured fields. Accounting checks decide whether they are ready for use. Missing or contradictory information reaches a review outcome with a reason, rather than automatically creating a financial record.

For example, the [unresolved supplier journey](../sample-case.md#purchase-invoice-review-required) preserves the document and extracted data while stopping before invoice creation.

## Posting and verification

The posting stage creates the appropriate Daftra record and attaches the source document where applicable. The documented payment path can receive a redirect after a save; it checks the saved record before reporting success. If the result cannot be confirmed, it requires reconciliation before retrying.

This separation distinguishes request completion from confirmed financial recording.

## Operator feedback

The upload/status interface exposes processing status. The activity log records the result or the stage and reason requiring attention. Supplier-selection cases require the operator to compare the selected account with the receipt beneficiary.

## Evidence from the supplied workflow

The [vector map](assets/workflow-map.svg) contains 132 processing nodes and 146 connections extracted from the supplied export. It preserves node positions and routes and omits one setup note. This provides structural evidence of the workflow; it does not show private node logic or verify execution.

## Additional evidence

| Artifact | What it would demonstrate |
| --- | --- |
| UI screenshot paired with a selected graph region | The operator experience alongside the corresponding workflow stage. |
| Close-up of validation and exception paths | How those documented checks are implemented. |
| Upload/status interface screenshot | The operator experience and visible states. |
| Reviewed, anonymized execution example | Input, observed decision, and resulting status from a real run. |

The additional artifacts in the table are not included yet. The existing fictional journeys explain expected behavior; they are not execution logs or automated tests.
