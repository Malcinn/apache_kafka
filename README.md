# distributed transaction

All applications are written with hexagonal architecture - designing software around business logic to isolate it from external factors. 

Application in hexagonal architecture consist of inside and outside parts.
* inside part - domain business logic
* outside part - rest of the code

In all services we will use 3 main packages:
* domain (inside) - business logic  - classes that models domain and also interfaces that define API to communicate with eternal parts like 
database with domain interfaces. 
* application (outside) - code that is responsible for all kind of interactions with application: CLI, REST API, Messaging, interfaces
* infrastructure (outside) - anything that application needs to work, db configuration, spring beans configuration, infrastructure dependent interfaces form domain layer 

Example project of distributed transactions.
order_service: save order on database and sends message to topic.
stock_service: listen for incoming messages and verifies the stock for the products in order.
transaction_service: Reveals API for distributed transaction mechanism.

