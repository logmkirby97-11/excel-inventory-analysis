# Inventory Health Analysis - Excel

**Status: In progress** — building this tab by tab.

## The business question
Across 5 stores with 20 products each, which items are tying up cash, which are at risk of
running out, and when should each specific item be reordered?

I'm approaching this as if I were working with an inventory manager who needs a reorder list and a view of where excess stock is sitting.

## Data
[Retail Store Inventory Forecasting Dataset](https://www.kaggle.com/datasets/anirudhchauhan/retail-store-inventory-forecasting-dataset)
(Kaggle, CC0). Synthetic data of about 73,000 daily records, Jan 2022 – Dec 2023.

## Progress
- [x] Imported and cleaned data in Power Query (raw data left alone)
- [x] Assumptions tab: lead time, service level, order and holding costs as named inputs
- [x] SKU summary: one row per store and product (100 unique SKU's)
- [ ] ABC/XYZ classification
- [ ] Inventory health (turnover, days of supply)
- [ ] Replenishment (safety stock, reorder point, EOQ)
- [ ] Forecast accuracy
- [ ] Dashboard and recommendations

## Cleaning decisions so far
- Set negative demand forecasts to 0 (a forecast can't be negative).
- Created a unique SKU
- Added a stockout flag column
- Using the initial date field, I created an additional weekly and monthly field

## Tools
Excel (Power Query, Excel Tables, SUMIFS/AVERAGEIFS, FILTER, UNIQUE, named ranges, data validation)