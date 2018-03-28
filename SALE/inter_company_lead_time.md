# 多公司环境前置期

* 客户提前期在多公司间共享
* 供应商提前期跟报价一起，不在多公司间共享
* 下文假设：
  * 香港公司从最终客户接单 (HSO)
  * 香港公司下单大陆公司 (HPO => DPO)
  * 大陆公司下单给最终供应商 (DPO)

指标 | 香港公司 | 大陆公司
-----|-----|-----
Customer Lead Time | 7 | 7
Manufacturing Lead Time | 1 | 1
Delivery Lead Time | 1 | N/A
Sales Safety Days* | 0 | 0
Manufacturing Lead Time* | 0 | 1
Purchase Lead Time* | 0 | 1

(*) 该指标在整个公司范围内适用

![HSO](_images/inter_company_lead_time5.PNG)

香港公司 `2018-03-07` 确认销售单，手动指定计划日期 `2018-04-23`。

![Vendor Lead Time](_images/inter_company_lead_time4.PNG)

香港公司设定供应商(大陆公司)前置期为1天。

![HPO](_images/inter_company_lead_time2.PNG)

```python
销售交货日期 - 公司的采购提前期 - 供应商交货提前期 = 采购订单日期
2018-04-23 - 0 - 1 = 2018-04-22
```

![HDO](_images/inter_company_lead_time3.PNG)

```python
采购订单日期 + 供应商交货提前期 = 入库单的计划日期
2018-04-22 + 1 = 2018-04-23
```

![DSO](_images/inter_company_lead_time.PNG)

```python
大陆公司销售订单日期 = 香港公司采购订单日期
2018-04-22 = 2018-04-22

大陆公司销售订单日期 = 大陆公司销售承诺日期 + 客户前置期
2018-04-22 + 7 = 2018-04-29
```