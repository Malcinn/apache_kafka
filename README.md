# distributed transaction


Example project of distributed transactions.
order_service: save order on database and sends message to topis.
stock_service: listen for incoming messages and verifies the stock for the products in order.
transaction_service: Reveals API for distributed transaction mechanism.

