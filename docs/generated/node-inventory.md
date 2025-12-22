---
architecture: ../architectures/ecommerce-platform.json
---
# Node Inventory: Microservices-based e-commerce platform for order processing, inventory management, and payments

| Name | Type | ID | Description |
|------|------|-------|-------------|
| Customer | Actor | `customer` | End customer using the e-commerce platform to browse and purchase products |
| Admin | Actor | `admin` | Administrator managing orders, inventory, and platform operations |
| API Gateway | Service | `api-gateway` | Central entry point for all client requests, providing routing, rate limiting, and request validation |
| Order Service | Service | `order-service` | Manages order creation, fulfillment, and tracking |
| Inventory Service | Service | `inventory-service` | Manages product inventory, stock levels, and availability |
| Payment Service | Service | `payment-service` | Handles payment processing, authorization, and settlement |
| Order Database | Database | `order-database` | Stores order data, including order history, status, and customer information |
| Inventory Database | Database | `inventory-database` | Stores product inventory, stock levels, and warehouse information |
| E-Commerce Platform | System | `ecommerce-platform` | Complete e-commerce platform comprising API gateway, microservices, and databases |

## Services Only

- **API Gateway** (`api-gateway`): Central entry point for all client requests, providing routing, rate limiting, and request validation
- **Order Service** (`order-service`): Manages order creation, fulfillment, and tracking
- **Inventory Service** (`inventory-service`): Manages product inventory, stock levels, and availability
- **Payment Service** (`payment-service`): Handles payment processing, authorization, and settlement

## Databases Only

- **Order Database** (`order-database`): Stores order data, including order history, status, and customer information
- **Inventory Database** (`inventory-database`): Stores product inventory, stock levels, and warehouse information

## Actors

- **Customer**: End customer using the e-commerce platform to browse and purchase products
- **Admin**: Administrator managing orders, inventory, and platform operations
