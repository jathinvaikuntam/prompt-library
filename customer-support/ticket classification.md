# Ticket Classification 

## Purpose
Automatically categorize incoming customer support tickets into predefined buckets so they can be routed to the right team without manual triage.

# task
zero-shot prompting
 
---

## Prompt

```
Classify the following customer support ticket into exactly one of these categories:
- Billing & Payments
- Technical Issue
- Account Access
- Shipping & Delivery
- Product Feedback
- Refund Request

Respond with only the category name, nothing else.

Ticket: """
{{TICKET_TEXT}}
"""
```

---

## Example Input

```
Ticket: """
Hi, I was charged twice for my order #4892 last Tuesday. I checked my bank statement
and there are two identical charges of  from your store. Please fix this .
"""
```

---

## Example Output

```
Billing & Payments
```