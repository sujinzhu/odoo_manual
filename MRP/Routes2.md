# Routes (Procurement)

Seq. | Route Name | Procurement Loc. | Source Loc. | Action | Move Supply Method
--- | --- | --- | --- | --- | ---
5 | Make To Order | Customers | DG/Stock | Move From Another Location | Create Procurement
10 | Supply by XXX (MTO) | DG/Stock | XXX | Move From Another Location | Create Procurement
15 | Manufacture | XXX | | Manufacture |
20 | Get from stock | XXX | DG/Stock | Move From Another Location | Take From Stock
20 | Get from stock (MTS) | XXX | DG/Stock | Move From Another Location | Create Procurement
25 | Buy | DG/Stock | | Buy |

(XXX refer to work shop, ether internal or subcontractor.)

Category | Category 2 | Route 1 | Route 2 | Route3
--- | --- | --- | ---- | ----
Trade | | Make To Order | Buy |
Finished Product | Assembly | Make To Order | Supply by Assembly (MTO) | Manufacture
Finished Product | Plastic | Make To Order | Supply by Plastic (MTO) | Manufacture
Finished Product | Cable | Make To Order | Supply by Cable (MTO) | Manufacture
Finished Product | Edgar | Make To Order | Supply by Edgar (MTO) | Manufacture
Finished Product | Sankyo | Make To Order | Supply by Sankyo (MTO) | Manufacture
Finished Product | Jiajie | Make To Order | Supply by Jinjia (MTO) | Manufacture
Raw Material | | Make To Order | Get from stock (MTO) | Buy
Raw Material | | | Get from stock | Buy

## 5. Make to Order

Minimum stock rule
> Minimum Stock rules are used to ensure that you always have the minimum amount of a product in stock in order to manufacture your products and/or answer to your customer needs. When the stock level of a product reaches its minimum the system will automatically generate a procurement with the quantity needed to reach the maximum stock level.

Make to Order
> The Make to Order function will trigger a Purchase Order of the amount of the Sales Order related to the product. The system will not check the current stock valuation. This means that a draft purchase order will be generated regardless of the quantity on hand of the product.

Minimum Stock rules and Make to Order
> The choice between the two options is thus dependent of your inventory strategy. If you prefer to have a buffer and always have at least a minimum amount, the minimum stock rule should be used. If you want to reorder your stocks only if your sale is confirmed it is better to use the Make to Order.

## 10. Supply by XXX (MTO)

XXX is internal work shop or subcontractor, for those products that are manfactured should choose one of such route. (Only one)

If none of these routes is chosen, MO will be generated at DG/Stock.

## 15. Manufacture

For those products that are manfactured **must** choose this rule.

## 20. Get from stock

For those products that are used in XXX and supply by DG/Stock, this rule or the next route should be chosen.

## 20. Get from stock (MTO)

For those products that are used in XXX and supply by DG/Stock, this rule or the previous route should be chosen.

## 25. Buy

For those products that are bought from supplier directly **must** choose this rule.