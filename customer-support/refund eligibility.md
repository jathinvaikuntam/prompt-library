# Refund Eligibility 

## Purpose
Reason through refund policy rules step-by-step before issuing a decision, reducing errors from  inconsistent judgments by support agents or automated missions.

# tags
chain of thought 
---

## Prompt

```
You are a support specialist applying our refund policy. Think through the case
step by step before giving a final decision.

Refund Policy Rules:
1. Full refund if item is returned within 30 days of delivery, unopened.
2. 50% refund if item is opened but defective and reported within 14 days.
3. No refund if damage is caused by the customer.
4. No refund after 30 days unless the item is defective.
5. Shipping costs are non-refundable unless the error was ours.

Customer Request:
"""
{{CUSTOMER_REQUEST}}
"""

Think through each relevant policy rule, state whether it applies, and explain why.
Then give a final decision: FULL REFUND / PARTIAL REFUND / NO REFUND, with the
exact amount if applicable and a one-sentence explanation to share with the customer.
```

---

## Example Input

```
Customer Request:
"""
I received my blender 10 days ago. I opened it, used it once, and the motor made a
loud grinding noise and then stopped working. I still have the original packaging.
Order total was 899 + 70 shipping.
"""
```

---

## Example Output

```
Step-by-step reasoning:

Rule 1 — Full refund (unopened, within 30 days): Item was opened. Does NOT apply.

Rule 2 — 50% refund (opened, defective, within 14 days): Item is opened ✓. Customer
reports a defect (motor failure) ✓. Reported within 14 days (day 10) ✓. APPLIES.
50% of 899 = 449.

Rule 3 — Customer-caused damage: Motor grinding on first use with original packaging
suggests a manufacturing defect, not misuse. Does NOT apply.

Rule 4 — No refund after 30 days: Only 10 days have passed. Does NOT apply.

Rule 5 — Shipping refund: The defect is a product issue, not a shipping error by us.
Shipping cost (70) is non-refundable.

FINAL DECISION: PARTIAL REFUND — 449
Customer message: "We're sorry your blender arrived with a motor defect — we'll
issue a 449 refund (50% per our opened-item defect policy) back to your payment
method within 5 business days."
```