# Final Insights

## 1. Business Impact
- Of 7,043 customers, **1,869 churned (26.54%)**. The retention rate is 73.46%.
- **Monthly revenue lost is 139,131, which is 30.5% of total monthly revenue** (about 1.67M per year).
- The revenue loss (30.5%) is higher than the customer loss (26.5%) because customers who churned paid more (average 74.4 vs 61.3 per month).
- Churned customers had an average tenure of 18 months vs 37.6 for retained customers (median 10 vs 38). Their average lifetime value was 1,339 vs 2,305.

## 2. Top Churn Drivers (ranked by Cramér's V)
| Rank | Factor | Cramér's V | Insight |
|---|---|---|---|
| 1 | Contract | 0.41 | Month-to-month 42.7%, one-year 11.3%, two-year 2.8% |
| 2 | Internet Service | 0.32 | Fiber optic 41.9%, DSL 19.0%, no internet 7.4% |
| 3 | Payment Method | 0.30 | Electronic check 45.3%, other methods 15-19% |
| 4 | Paperless Billing | 0.19 | Paperless 33.6% vs 16.3% |
| 5 | Online Security / Tech Support | 0.17 / 0.16 | About 31% churn without them, about 15% with them |

All factors are statistically significant (p < 0.05) except gender (p = 0.49) and phone service (p = 0.34).

## 3. Contract and Revenue
- **About 87% of lost revenue (120,847 of 139,131) comes from month-to-month customers.**
- One-year contracts lost 14,118 and two-year contracts lost only 4,165.

## 4. Tenure (The First Year)
- Churn is **47.4%** in months 0-12, 28.7% in months 13-24, 20.4% in months 25-48 and only 9.5% after 49 months.
- **Month 1 alone loses 22,115 in monthly revenue (about 16% of the total).** The first 12 months account for about 50% of all lost revenue.
- This points to an onboarding and early-experience problem.

## 5. Services
- **Tech support:** 31.2% churn without it vs 15.2% with it.
- **Online security:** 31.3% churn without it vs 14.6% with it.
- Online backup (29.2% vs 21.5%) and device protection (28.7% vs 22.5%) have a smaller effect.
- Streaming TV and movies customers churn slightly more (about 30% vs 24%), but the effect is small (V ≈ 0.06). It is probably linked to fiber and higher prices.
- Customers with more services tend to churn less. Note that the "0 services" group includes customers with no internet, who rarely churn, so it should be read separately.

## 6. Customer Profile
- **Senior citizens churn at 41.7%** vs 23.6% for non-seniors.
- **Customers without a partner churn at 33.0%** (19.7% with a partner). **Customers without dependents churn at 31.3%** (15.5% with dependents).
- **Gender has no significant effect on churn.**

## 7. Price
- Churned customers had a median monthly charge of 79.65 vs 64.43 for retained customers (p < 0.001). Higher-paying customers are more likely to leave.

## 8. High-Risk Segment
Month-to-month contract + fiber optic + tenure of 12 months or less + no tech support:
- **833 customers (11.8% of the base)**
- **71.1% churn rate**, about 2.7x the overall rate of 26.5%
- **31.7% of all churn**, and 48,490 of monthly revenue lost (about 35% of the total loss)
- This is the first group to target with retention offers.

## 9. Predictive Model
- All three models perform almost identically on the test set: Logistic Regression 0.844, Random Forest 0.845, Gradient Boosting 0.843 ROC-AUC (cross-validated AUC about 0.85).
- Random Forest **caught 78% of churners (recall)** with 54% precision at the default 0.5 cutoff.
- Feature engineering moved AUC only from 0.842 to 0.844, so most of the signal was already in the original features.
- **Contract is the most important feature (0.036), followed by tenure (0.010).** Electronic check and tech support do not appear in the model's top features because they overlap with contract and tenure.
- **The top 20% of customers ranked by risk contain 50% of all churners (2.5x lift)**, and the top 40% contain 79.7%.

## 10. Recommendations
1. **Offer annual-contract discounts to month-to-month customers.** They are the source of about 87% of lost revenue.
2. **Give new fiber customers free tech support or online security in their first year.**
3. **Run an onboarding campaign for the first 3 months** (welcome call, usage check-in).
4. **Move electronic check customers to auto-pay** with a small discount or cashback.
5. **Send retention offers to the top 20% of customers by model risk score.** Half of all churners are in this group.
6. **Create tailored plans or support for senior and single-person households.**

## 11. Limitations
- The dataset is a snapshot (no date column), so time trends cannot be analyzed.
- These results show correlation, not causation. Retention offers should be A/B tested.
- The offer cost and success rate used in the business-impact step are assumptions.
- Data on complaints, call-center interactions and competitor offers is not available.
