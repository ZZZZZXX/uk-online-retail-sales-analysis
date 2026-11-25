# Project Summary

## English Summary

This portfolio project analyses the UCI Online Retail dataset through Python, pandas, matplotlib, Jupyter and Excel, covering transaction data quality, monthly sales patterns, customer activity and product-code sales concentration. It is **descriptive analysis**, not a model of profitability, causality, demand forecasting or inventory optimisation.

- **Raw input:** 541,909 invoice lines.
- **Early analysed subset:** 397,884 eligible invoice lines after filtering to `Quantity > 0`, `UnitPrice > 0` and non-null `CustomerID`. This subset has £8,911,407.90 in recorded sales value (`Quantity × UnitPrice`), 18,532 distinct invoices and 4,338 identified customers.
- **Monthly patterns:** Recorded sales value, order counts and identified customer activity were higher during September–November 2011; November was the peak month in this period. December 2011 is incomplete. These co-occurring movements do not establish why sales changed.
- **Product-code concentration (two historical definitions, same early transaction subset):**
  - **78.65%** — top 20% of all **3,665** `StockCode` values, including special entries such as postage and fees (top **733** codes). Saved in the [historical root notebook](https://github.com/ZZZZZXX/uk-online-retail-sales-analysis/blob/41ec18ec80a17b9243cfc22edca37c310b312439/01_data_loading.ipynb).
  - **78.38%** — top 20% of **3,660** `StockCode` values after excluding specified non-product/special entries (top **732** codes). Saved in the [current notebook](../notebooks/01_data_loading.ipynb). This is the **product-concentration figure used in the NTU CV**.
  - Exclusion list: `POST`, `M`, `D`, `DOT`, `BANK CHARGES`, `AMAZONFEE`, `CRUK`, `C2`, `S`. Only some of these codes were present in the analysed subset.
- **Later reconciliation:** A [separate revised project](https://github.com/ZZZZZXX/-uci-online-retail-business-analytics) reports **78.32%** for the top 20% of 3,790 normalized merchandise codes, based on updated transaction eligibility and merchandise definitions. It is **not a like-for-like comparison** with the early figures and reflects later, tool-assisted work. That later project also reports that **16.49%** of gross completed-sales value came from rows with missing customer identifiers.

**How to interpret the figures:** The historical analyses confirm strong concentration of recorded sales value among product codes, but the dataset lacks product margin, cost, stock and fulfilment information. These measures cannot establish the best inventory policy, customer lifetime value or actual business impact. The results should inform questions for further investigation, not be represented as implemented inventory recommendations.

**Excel deliverables:** The early repository's notebook exports a filtered **flat worksheet** named `Online_Retail_Dashboard.xlsx`. An initial Excel dashboard was also created during the project, but that original standalone dashboard is not published as a reproducible file here. The [later reconciled project](https://github.com/ZZZZZXX/-uci-online-retail-business-analytics) includes a larger multi-sheet Excel dashboard created/repaired in its own later workflow. Do not treat these as identical artifacts or assume all later improvements were independently written in the early project.

## 中文项目总结

本项目基于 UCI Online Retail 的 **541,909 条原始发票明细**，使用 Python、pandas、Jupyter、matplotlib 与 Excel，进行数据检查、清洗、核心指标计算、月度趋势及商品销售价值集中度的描述性分析。

- **早期分析总体：** 保留数量和价格均为正、且 CustomerID 非空的 397,884 条明细；记录销售价值为 £8,911,407.90，涉及 18,532 张不同发票、4,338 位已识别客户。
- **月度趋势：** 2011 年 9–11 月观察到销售价值、订单数及活跃客户数量的较高水平，11 月达到峰值；12 月只有部分月份数据。这些是同时发生的描述性变化，**不能据此证明因果关系**。
- **两种商品代码口径：**
  - 包含全部 3,665 个 StockCode（其中可能包含邮费、服务费等特殊代码），前 20% 即 733 个代码的销售价值占比为 **78.65%**；
  - 排除事先列出的非商品/特殊代码后，剩余 3,660 个 StockCode，前 20% 即 732 个代码的销售价值占比为 **78.38%**（**NTU CV 使用这一口径**）。
  - 两者使用相同的早期交易筛选规则，差别是商品代码是否纳入排名及销售价值分母，并非数据算错。
- **后续项目复核：** 采用不同交易与规范化商品定义的版本得到 **78.32%**，并发现缺失 CustomerID 的完成销售对应全部完成销售价值的 **16.49%**。这一后期口径不能仅理解为“排除非商品代码”这一项变化。
- **结论边界：** 这些指标可用于确定进一步调查的方向，但原始数据不含商品毛利、库存水平、履约与干预结果，不能证明库存优化、盈利改善或供应链决策已实际落地。
- **Excel 文件归属：** 早期 Notebook 公开的是将筛选后数据导出为单表的 Excel 文件；本人曾制作初版 Excel 看板，但该独立原始文件并未作为可复现产物发布在本早期仓库。后期多工作表看板属于另一个修订项目的成果，不应混同为早期独立完成的版本。

## Suggested accurate CV wording / 建议使用的 CV 事实边界

- Analysed 541,909 raw invoice lines using Python and pandas; after filtering transactions and excluding specified non-product codes, the top 20% of 3,660 StockCodes accounted for 78.38% of sales value in the analysed subset.
- Reviewed a later reconciliation under revised sales and merchandise definitions (78.32%), assessing how customer-identity and product-code rules shape the interpretation of sales concentration.
- Created an initial Excel dashboard and matplotlib visualisations; documented descriptive findings, assumptions, and limits arising from unavailable margin and inventory data in a written report.

The work does **not** substantiate quantified inventory improvements, completed forecasting, causal effects or claims that an employer acted on the retail analysis.
