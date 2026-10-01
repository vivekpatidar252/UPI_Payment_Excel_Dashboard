# UPI Transactions Analysis Report

**Prepared by:** Vivek Patidar
**Tool:** Microsoft Excel (Pivot Tables, Slicers, Charts)
**Deliverable:** Interactive dashboard (`Project` sheet)

---

## 1. Objective

To analyse UPI transaction data and answer a few practical questions:

- How many transactions happen, and what is their total value?
- How reliable are payments (success, failure, pending, fraud)?
- Which transaction types, banks and states drive the most value?
- When during the day do people pay the most?
- Who is spending: which gender and age group?

## 2. Dataset

Raw UPI transaction records (about 5 lakh rows) with fields such as merchant name, merchant category, city, state, bank, gender, age group, transaction type, status, amount, cashback and time of transaction.

## 3. Approach

1. Loaded the raw data into Excel and cleaned it for analysis.
2. Built Pivot Tables for each view (type, status, bank, state, hour, gender, age group, daily trend).
3. Created Pivot Charts and a map chart from those tables.
4. Designed KPI cards for the headline numbers.
5. Added slicers (Merchant Name, Gender, Merchant Category, City) so every chart responds to one set of filters.

## 4. Headline Numbers

| Metric | Value |
|---|---|
| Total Transactions | 5,02,887 |
| Total Amount | about ₹4.4 Cr |
| Total Cashback | ₹19 L |
| Success Rate | 91.00% |
| Fraud Rate | 3.40% |

## 5. Findings

### 5.1 Transaction type

| Type | Share of transactions |
|---|---|
| P2M (merchant payments) | 42.66% |
| P2P | 19.83% |
| Bill Payment | 13.95% |
| Online Shopping | 8.66% |
| Recharge | 7.99% |
| Subscription | 4.06% |
| Wallet Transfer | 2.85% |

P2M is the dominant category, and by amount it is also the largest (about ₹1.89 Cr), followed by P2P (about ₹0.88 Cr) and Bill Payment (about ₹0.62 Cr).

### 5.2 Payment status

- Success: 91.00%
- Failed: 6.95%
- Pending: 1.96%

Roughly 9 in every 100 payments do not complete on the first attempt.

### 5.3 Banks

All eight banks fall in a narrow band of about ₹51 L to ₹59 L. HDFC Bank (about ₹58.9 L) and SBI (about ₹58.4 L) lead, while Punjab National Bank is lowest (about ₹51.1 L).

### 5.4 Time of day

Payment value rises from early morning, shows a bump around noon, and peaks between 5 PM and 8 PM (highest at 7 PM). It falls sharply after 9 PM and is lowest in the late-night hours.

### 5.5 Gender and age

- Male users: about ₹2.40 Cr
- Female users: about ₹1.98 Cr
- The 25-34 age group contributes the largest share of spend.

### 5.6 States

Most states in the top list sit between ₹41 L and ₹45 L, so spending is spread fairly evenly. Kerala shows a much lower value (about ₹1.39 L) and should be verified against the source data.

## 6. Recommendations

1. **Focus on merchant payments.** P2M is the growth driver, so merchant offers and cashback are likely to have the most impact.
2. **Reduce failures.** A 6.95% failure rate and 1.96% pending are worth targeting with retry flows and better bank-side success rates.
3. **Time campaigns for the evening.** Promotions and cashback pushes around 5-8 PM would reach users when they are most active.
4. **Monitor fraud.** At 3.40%, fraud should be tracked by category, bank and time of day to find where it concentrates.
5. **Target the 25-34 group.** They are the largest spending segment.

## 7. Limitations

- The analysis is descriptive and based on one dataset, so it does not show causes.
- Percentages are read from the dashboard and rounded.
- The Kerala value looks like an outlier and needs a data check.

## 8. Tools Used

Microsoft Excel: Pivot Tables, Pivot Charts, Slicers, Map Chart, KPI cards.

---

*Dashboard screenshot: see `dashboard.png` in the repository.*
