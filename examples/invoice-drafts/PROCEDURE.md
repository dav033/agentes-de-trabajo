---
schema_version: 1
---
# Synthetic procedure

1. Validate that the supplied case identifies the currency, quantity, unit price, line discounts and tax treatment. Missing material fields remain explicit questions.
2. Use integer minor units, with the currency's minor-unit definition explicit. This synthetic USD case uses cents. Do not mix currencies.
3. Compute line net as quantity times unit price minus the supplied line discount. Add only explicitly supplied taxes. Check discount bounds and quantities before computing.
4. Present a draft with case reference, lines, totals, currency and missing information. Mark it “Borrador — no emitido”. Do not generate a legally assigned invoice number.
5. Let the owner review it. Remember a confirmed presentation preference within its scope; treat a tax/approval/process change as a proposal needing approval.

## Synthetic fixture and expected arithmetic

Case `DEMO-001`; fictitious customer `Cliente de ejemplo`; currency USD, 100 cents per dollar. Quantity 2; unit price 1500 cents; total line discount 200 cents; explicitly supplied tax 0 cents for this fictional arithmetic exercise. Expected net and total: 2800 cents = USD 28.00. Zero tax here is fixture data, not legal or production tax guidance.

## Readiness

No actual owner has accepted this procedure. The arithmetic fixture alone does not demonstrate a live Work run, invoice integration or production readiness. Keep this example draft and outside the active registry.
