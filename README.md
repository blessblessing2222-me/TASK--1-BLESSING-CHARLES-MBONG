# TASK--1-BLESSING-CHARLES-MBONG
DECODELAPS MARCH INTERN PROJECT-1-DATA-CLEANING-PREPARATORY
# DATA-CLEANING & PREPARATION

# Part 1 — Noise Analysis: Data Integrity Verification

After a comprehensive integrity audit across all 1,200 records, *zero data entry errors were detected.*

| Check | Result |
|---|---|
| Arithmetic Consistency (Quantity × UnitPrice = TotalPrice) | ✅ Perfect match across all records |
| Categorical Integrity (Products, Payment Methods, Order Status, Referral Source) | ✅ No typos or label inconsistencies |
| Duplicate Records (OrderID) | ✅ All records are unique |

#Conclusion:* No records require removal or correction. The dataset is clean and ready for downstream analysis.

---

### Part 2 — Signal Analysis: Insights & Opportunities

While the data requires no cleaning, it contains meaningful signals worth investigating.

#### 🏷️ High-Value Transactions — VIP Customer Potential

Statistical outlier detection (IQR method) identified *8 transactions* that fall significantly above the normal TotalPrice range, with order values reaching *~$3,300+*.

| Order ID | Product | Total Price |
|---|---|---|
| ORD200107 | Printer | $3,353.75 |
| ORD200326 | Laptop | $3,352.40 |
| ORD200328 | Tablet | $3,370.20 |
| ORD200469 | Chair | $3,384.90 |
| ORD200632 | Laptop | $3,390.80 |
| (+ 3 additional records) | — | — |

# *Recommended Action:* Cross-reference these transactions against your CRM to determine whether they represent legitimate bulk purchases by VIP customers or warrant a fraud review (e.g., check for rapid cancellations or unusual payment method patterns).

---

#### 🎟️ Coupon Usage — Marketing Behaviour Segmentation

The CouponCode column contains NaN (missing) values, which are *not errors* — they are a behavioural signal indicating customers who purchased without a promotional code.

# *Recommended Action:* Conduct a segmentation analysis comparing coupon users vs. non-coupon users across the following dimensions:

> - Average order value and purchase frequency
> - ReferralSource distribution
> - OrderStatus outcomes (e.g., completion vs. cancellation rates)
>
> 
# This analysis can reveal whether coupon-free customers represent a higher-value segment and inform future marketing spend decisions.

---

Report generated as part of the Decodelap Data Analytics Internship — Batch 2026.

# AUTHOR
# Blessing Charles 
📍  Nigeria
# 🔗 https://www.linkedin.com/in/blessing-charles-b4877063

