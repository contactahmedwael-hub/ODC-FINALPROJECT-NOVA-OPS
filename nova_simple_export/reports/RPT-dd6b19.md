# Nova Retail Weekly Operations Report

## Executive summary
The retailer faces urgent stockouts for three key items: an Ergonomic Office Chair with limited stock and a high risk of shortage, a USB-C Hub experiencing rapid demand increase and delivery delays, and a Wireless Mouse facing increased customer complaints due to supply issues.

## Sales - last 7 days
In the last seven days, revenue decreased by 8.9% compared to the previous week, totaling $5,432.01 from 84 orders, with an average order value of $64.67. Key products contributing to sales were the USB-C Hub, Wireless Mouse, and Notebook 3-Pack.

| Top product | Revenue | Units |
|---|---|---|
| USB-C Hub | $1,399.65 | 35 |
| Wireless Mouse | $949.62 | 38 |
| Ergonomic Office Chair | $749.95 | 5 |
| Notebook 3-Pack | $589.41 | 59 |
| Backpack | $539.88 | 12 |

## Inventory risk
At the end of September 2026, the retailer had critical risks for Ergonomic Office Chair and Gel Pen Set with low stock levels and high reorder quantities, while Reusable Water Bottle faced medium risk due to above-reorder level stock. USB-C Hub and Notebook 3-Pack were flagged as high-risk items with significant safety stock needed, but Wireless Mouse and Backpack were at lower risk with adequate inventory.

| Product | Risk | Stock | Days of stock | Lead time | Draft reorder |
|---|---|---|---|---|---|
| Ergonomic Office Chair | critical | 2 | 3.8 | 28 | 21 |
| Gel Pen Set | critical | 40 | 4.9 | 7 | 133 |
| USB-C Hub | critical | 45 | 7.8 | 14 | 116 |
| LED Desk Lamp | high | 33 | 11.4 | 10 | 37 |
| Wireless Mouse | high | 75 | 15.7 | 14 | 59 |
| Reusable Water Bottle | medium | 70 | 17.4 | 12 | 35 |

**Assumptions**
- Daily demand = units sold in the last 30 days / 30; assumed to continue unchanged.
- Safety buffer = 3 days on top of supplier lead time.
- Draft reorder qty = demand x (lead time + 14 days) - stock; needs human review.

## Customer feedback
The retailer received 100 feedback items with an average rating of 3.61. Customers reported significant issues with product availability and delivery, with 15 out of 22 availability-related comments being negative and 12 out of 13 delivery-related comments being negative. Quality concerns were less frequent, with only 4 out of 15 negative comments.

- Hypothesis: availability complaints may be linked to low stock or long lead times (not verified).
- Hypothesis: delivery complaints may come from carrier or supplier delays (not verified).
- Hypothesis: repeated quality complaints may point to a defective batch (not verified).

## Proposed actions (need approval)
- **[high] Urgent: possible stockout of Ergonomic Office Chair (P004)** - Ergonomic Office Chair: stock 2; 3.8 days of stock vs 28-day supplier lead time. Evidence: inventory:P004, sales:P004, doc:supplier_terms.pdf p.1. Next: Confirm lead time with Delta Home Supplies and approve or edit the draft purchase review. Suggested draft quantity: 21 units (needs review).
- **[high] Urgent: possible stockout of USB-C Hub (P002)** - USB-C Hub: stock 45; 7.8 days of stock vs 14-day supplier lead time; 10 customer complaints about availability/delivery. Evidence: inventory:P002, sales:P002, feedback:F009, feedback:F039, feedback:F050, doc:supplier_terms.pdf p.1. Next: Confirm lead time with Nile Tech Distribution and approve or edit the draft purchase review. Suggested draft quantity: 116 units (needs review).
- **[high] Urgent: possible stockout of Wireless Mouse (P001)** - Wireless Mouse: stock 75; 15.7 days of stock vs 14-day supplier lead time; demand up 21% over the last 14 days vs the 14 before; 6 customer complaints about availability/delivery. Evidence: inventory:P001, sales:P001, feedback:F011, feedback:F023, feedback:F029, doc:supplier_terms.pdf p.1. Next: Confirm lead time with Nile Tech Distribution and approve or edit the draft purchase review. Suggested draft quantity: 59 units (needs review).
- **[medium] Urgent: possible stockout of Gel Pen Set (P006)** - Gel Pen Set: stock 40; 4.9 days of stock vs 7-day supplier lead time; 12 customer complaints about availability/delivery. Evidence: inventory:P006, feedback:F007, feedback:F014, feedback:F022, doc:supplier_terms.pdf p.2. Next: Confirm lead time with BrightSource Wholesale and approve or edit the draft purchase review. Suggested draft quantity: 133 units (needs review).
- **[medium] Investigate recurring quality complaints for product P003** - 4 quality complaints, average rating 2.0. Evidence: feedback:F024, feedback:F025, feedback:F042, feedback:F093. Next: Inspect stock for defects and review with the supplier (see defect terms in the supplier PDF).
- **[low] Review reorder for LED Desk Lamp (P003)** - LED Desk Lamp: stock 33; 11.4 days of stock vs 10-day supplier lead time. Evidence: inventory:P003, doc:supplier_terms.pdf p.1. Next: Confirm lead time with Delta Home Supplies and approve or edit the draft purchase review. Suggested draft quantity: 37 units (needs review).

## Verification
Passed: True (73 checks). 

---
DRAFT - NOT SENT. Review and edit; this program never sends emails or places orders.