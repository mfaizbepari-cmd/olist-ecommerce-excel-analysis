Orders
Grain: One row per order
Primary identifier: order_id

Order Items
Grain: One row per product line within an order
Identifier: order_id + order_item_id

Payments
Grain: One payment record associated with an order
Identifier: order_id + payment_sequential

Products
Grain: One row per product
Identifier: product_id