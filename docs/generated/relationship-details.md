---
architecture: ../architectures/ecommerce-platform.json
---
# Relationship Details: Microservices-based e-commerce platform for order processing, inventory management, and payments

### customer-interacts-api-gateway


**Type:** Interaction

- **Actor:** `customer`
- **Interacts with:** `api-gateway`


---
### admin-interacts-api-gateway


**Type:** Interaction

- **Actor:** `admin`
- **Interacts with:** `api-gateway`


---
### api-gateway-connects-order-service

**Type:** Connection

| Property | Value |
|----------|-------|
| Source | `api-gateway` |
| Destination | `order-service` |
| Source Interfaces | `api-gateway-https` |
| Dest Interfaces | `order-service-api` |



---
### api-gateway-connects-inventory-service

**Type:** Connection

| Property | Value |
|----------|-------|
| Source | `api-gateway` |
| Destination | `inventory-service` |
| Source Interfaces | `api-gateway-https` |
| Dest Interfaces | `inventory-service-api` |



---
### order-service-connects-order-database

**Type:** Connection

| Property | Value |
|----------|-------|
| Source | `order-service` |
| Destination | `order-database` |
| Source Interfaces | `order-service-api` |
| Dest Interfaces | `order-database-jdbc` |



---
### order-service-connects-payment-service

**Type:** Connection

| Property | Value |
|----------|-------|
| Source | `order-service` |
| Destination | `payment-service` |
| Source Interfaces | `order-service-api` |
| Dest Interfaces | `payment-service-api` |



---
### inventory-service-connects-inventory-database

**Type:** Connection

| Property | Value |
|----------|-------|
| Source | `inventory-service` |
| Destination | `inventory-database` |
| Source Interfaces | `inventory-service-api` |
| Dest Interfaces | `inventory-database-jdbc` |



---
### ecommerce-platform-composed-of-services



**Type:** Composition

- **Container:** `ecommerce-platform`
- **Contains:** `api-gateway`, `order-service`, `inventory-service`, `payment-service`, `order-database`, `inventory-database`

---
