Olist Brazilian E-Commerce — End-to-End Analysis
My first end-to-end data project: cleaning, exploratory analysis and customer
segmentation on ~100,000 real e-commerce orders using Python, Pandas and Matplotlib.

Author: Kartikeya Solanki — Aspiring Data & Product Analyst
(BS Data Science & Applications, IIT Madras · BS Digital Science & Business Management, IIM Mumbai)

Dataset
Source: Brazilian E-Commerce Public Dataset by Olist (Kaggle)
Size: ~100k orders (2016–2018), real commercial data, anonymized by Olist
(company/partner names in reviews were replaced with Game of Thrones house names)
License: CC BY-NC-SA 4.0 —
attribution to Olist required; non-commercial use. This repo is an educational project
with full attribution.
Files: 9 CSVs — orders, order items, payments, reviews, products, sellers,
customers, geolocation, category name translation.
Download the CSVs from Kaggle into a local data/ folder (not committed to git —
see .gitignore). No API key is needed if you download via browser; kaggle
CLI also works: kaggle datasets download -d olistbr/brazilian-ecommerce.

Questions answered
How does monthly revenue trend over 2016–2018? (Found: clear November 2017
spike — Black Friday week; note the Sep–Oct 2018 drop is the dataset's
coverage ending, not a demand crash.)
Which product categories drive order volume?
How do customers pay? (Credit card vs boleto vs voucher vs debit card)
Which states do orders come from?
What do customers look like under RFM segmentation
(New / One-time regulars / At-risk / Loyal)?
Key findings
Revenue grew strongly through 2017; Black Friday week (Nov 2017) visibly
lifted the entire month.
Everyday categories (bed & bath, health & beauty, sports & leisure) lead
order volume — not electronics.
Credit card dominates payments (~3 of 4 orders); boleto (Brazil's bank-slip
system) is still ~1 in 5.
São Paulo, Rio de Janeiro and Minas Gerais account for roughly 2 of every 3 orders.
Most customers buy exactly once — the Loyal segment is small, so retention
looks like the biggest growth lever.
Repo structure
text

├── notebooks/
│   └── 01_olist_eda_rfm.ipynb      # cleaning → EDA → RFM, fully commented
├── charts/                         # Matplotlib exports used in the LinkedIn carousel
├── data/                           # CSVs go here (not committed)
└── README.md

How to run
Bash

pip install pandas matplotlib jupyter
jupyter notebook notebooks/01_olist_eda_rfm.ipynb

Tools
Python · Pandas · Matplotlib · Jupyter

What I learned
1.Data cleaning took ~60% of the total time — not modeling.
2.Simple bar charts communicated findings better than complex plots.
3.Documenting assumptions mattered more than fancy code.
