# Lead Time

## 参考

* (销售) [Delivery Lead Time](SALE/delivery_lead_time.md)
* [多公司环境前置期](SALE/inter_company_lead_time.md)
* (制造) [Manufacturing Lead Time](MRP/manufacturing_lead_time.md)
* (采购) [Purchase Lead Time](PUR/purchase_lead_time.md)
* [Glossary 术语表](glossary.md)

## 术语

单据 | 术语 | 翻译 | 意义
----- | ----- | ----- | -----
Sales Order | Order Date | 单据日期 |
Sales Order | Creation Date | 创建日期 |
Sales Order | Expiration Date | 过期日期 |
Sales Order | Confirmation Date | |
Sales Order | Requested Date | 要求日期 |
Sales Order | Commitment Date | 承诺日期 |
Sales Order | Effective Date | 实际日期 |

## 设定

指标 | 香港公司 | 大陆公司
-----|-----|-----
Customer Lead Time | 115 | 115
Manufacturing Lead Time | 0 | 0
Delivery Lead Time | 1 | N/A
Sales Safety Days* | 0 | 0
Manufacturing Lead Time* | 0 | 1
Purchase Lead Time* | 0 | 1

## 验证

单据 | 字段 | 值
----- | ----- | -----
Sales Order | Order Date | `2018-03-16`
Sales Order | Creation Date | `2018-03-29`
Sales Order | Expiration Date | 
Sales Order | Confirmation Date | `2018-03-29`
Sales Order | Requested Date | 
Sales Order | Commitment Date | `2018-007-09`
Sales Order | Effective Date | 
Delivery Order | Schedule Date | `2018-07-09`

```python
Order Date + Customer Lead Time ( + Sales Safety Days* )= Commitment Date
2018-3-16 + 115 ( + 0 ) = 2018-7-9
```