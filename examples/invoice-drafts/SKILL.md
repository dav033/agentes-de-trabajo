---
name: invoice-drafts
description: "Prepare synthetic invoice drafts from supplied order data for an owner to review. This example does not issue invoices, submit taxes or contact customers."
metadata:
  schema_version: "1"
  version: "0.1.0"
  state: "draft"
---
# Borradores de facturas — synthetic example

This is an authoring example, outside the active registry. No actual owner acceptance, Work installation or live connection is claimed. Read [procedure](PROCEDURE.md), [memory](MEMORY.md), [decisions](DECISIONS.md) and [pending work](PENDING.md).

Prepare a reviewable draft using supplied, validated order data. Label it “Borrador — no emitido”. Use explicit currency and units; never infer tax rates, legal validity, customer identifiers or source-system balances. Do not invent missing commercial data.

The coordinator checks lifecycle, workspace grants and real connections before execution. Follow its memory/persistence rules. No email, invoice issuance, tax submission, accounting write, business approval or remote-write grant exists in this example.

Required mode: manual synthetic draft from supplied input; no external connection. A future live-order lookup is a new connection requirement to discover and propose before depending on it.
