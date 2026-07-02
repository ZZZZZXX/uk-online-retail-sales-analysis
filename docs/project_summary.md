# Project Summary

## English Summary

UK Online Retail Sales Data Analysis is a business analytics project based on the UCI Online Retail dataset. The project cleans transaction-level retail data, calculates core business KPIs, analyzes monthly sales and order trends, studies customer activity, and evaluates product revenue concentration.

After cleaning, the dataset contains 397,884 valid transaction records from 541,909 raw transaction rows. The cleaned sales data shows approximately £8.91M in total revenue, 18,532 orders, 4,338 customers, and 3,665 products. Sales increased significantly from September to November 2011 and peaked in November. The growth pattern was mainly supported by increased order volume and active customer activity.

The analysis also shows that product revenue is highly concentrated. Using StockCode as the product identifier, the top 20% of products contributed 78.65% of total revenue. Product contribution was calculated using StockCode as the product identifier. Results may vary slightly if products are grouped by Description or by StockCode-Description pairs.

## 中文简历项目描述

基于 UCI Online Retail 数据集完成英国线上零售销售数据分析项目，使用 Python、pandas、matplotlib 和 Excel 对 541,909 条交易记录进行数据清洗、指标计算和可视化分析。清洗后保留 397,884 条有效交易记录，分析总销售额约 £8.91M、18,532 个订单、4,338 名客户和 3,665 种商品，并从月度销售趋势、订单量、活跃客户、商品贡献度和 Pareto 分析角度提炼业务洞察。结果显示销售额在 2011 年 9 月至 11 月显著增长，并于 11 月达到峰值，增长主要由订单量和活跃客户数量提升驱动。

## 中文简历要点

- 使用 Python 和 pandas 清洗 UCI Online Retail 交易数据，剔除缺失客户 ID、退货/取消订单、无效数量和非正价格记录，保留 397,884 条有效销售记录用于后续分析。
- 构建核心业务 KPI，统计总销售额约 £8.91M、18,532 个订单、4,338 名客户和 3,665 种商品，形成可用于业务汇报的指标摘要。
- 分析月度销售额、订单量和活跃客户趋势，发现 2011 年 9 月至 11 月销售显著增长并在 11 月达到峰值，判断增长主要由订单量和客户活跃度提升驱动。
- 使用 StockCode 作为商品标识进行 Pareto 分析，验证核心商品收入集中度：Using StockCode as the product identifier, the top 20% of products contributed 78.65% of total revenue.
