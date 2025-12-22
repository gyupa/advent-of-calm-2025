---
id: index
title: Welcome to CALM Documentation
sidebar_position: 1
slug: /
---

# Welcome to CALM Documentation

This documentation is generated from the **CALM Architecture-as-Code** model.

## High Level Architecture
```mermaid
C4Deployment

    Deployment_Node(deployment, "Architecture", ""){
        Person(customer, "Customer", "End customer using the e-commerce platform to browse and purchase products")
        Person(admin, "Admin", "Administrator managing orders, inventory, and platform operations")
        Deployment_Node(ecommerce-platform, "E-Commerce Platform", "Complete e-commerce platform comprising API gateway, microservices, and databases"){
            Container(api-gateway, "API Gateway", "", "Central entry point for all client requests, providing routing, rate limiting, and request validation")
            Container(order-service, "Order Service", "", "Manages order creation, fulfillment, and tracking")
            Container(inventory-service, "Inventory Service", "", "Manages product inventory, stock levels, and availability")
            Container(payment-service, "Payment Service", "", "Handles payment processing, authorization, and settlement")
            Container(order-database, "Order Database", "", "Stores order data, including order history, status, and customer information")
            Container(inventory-database, "Inventory Database", "", "Stores product inventory, stock levels, and warehouse information")
        }
    }

    Rel(customer,api-gateway,"Interacts With")
    Rel(admin,api-gateway,"Interacts With")
    Rel(api-gateway,order-service,"Connects To")
    Rel(api-gateway,inventory-service,"Connects To")
    Rel(order-service,order-database,"Connects To")
    Rel(order-service,payment-service,"Connects To")
    Rel(inventory-service,inventory-database,"Connects To")

    UpdateLayoutConfig($c4ShapeInRow="3", $c4BoundaryInRow="2")
```
## Nodes
    - [Customer](nodes/customer)
    - [Admin](nodes/admin)
    - [API Gateway](nodes/api-gateway)
    - [Order Service](nodes/order-service)
    - [Inventory Service](nodes/inventory-service)
    - [Payment Service](nodes/payment-service)
    - [Order Database](nodes/order-database)
    - [Inventory Database](nodes/inventory-database)
    - [E-Commerce Platform](nodes/ecommerce-platform)

## Relationships
    - [Customer Interacts Api Gateway](relationships/customer-interacts-api-gateway)
    - [Admin Interacts Api Gateway](relationships/admin-interacts-api-gateway)
    - [Api Gateway Connects Order Service](relationships/api-gateway-connects-order-service)
    - [Api Gateway Connects Inventory Service](relationships/api-gateway-connects-inventory-service)
    - [Order Service Connects Order Database](relationships/order-service-connects-order-database)
    - [Order Service Connects Payment Service](relationships/order-service-connects-payment-service)
    - [Inventory Service Connects Inventory Database](relationships/inventory-service-connects-inventory-database)
    - [Ecommerce Platform Composed Of Services](relationships/ecommerce-platform-composed-of-services)


## Flows
    - [Customer Order Processing](flows/order-processing-flow)
    - [Inventory Stock Check](flows/inventory-check-flow)

## Controls
| Requirement URL               | Category    | Scope        | Applied To                |
|-------------------------------|-----------|--------------|---------------------------|
|https://internal-policy.example.com/performance/rate-limiting|performance|Node|api-gateway|
|https://www.pcisecuritystandards.org/documents/PCI-DSS-v4.0|compliance|Node|payment-service|

## Metadata
  <div className="table-container">
      <table>
          <thead>
          <tr>
              <th>Key</th>
              <th>Value</th>
          </tr>
          </thead>
          <tbody>
          <tr>
              <td>
                  <b>Owner</b>
              </td>
              <td>
                  Gyula
                      </td>
          </tr>
          <tr>
              <td>
                  <b>Version</b>
              </td>
              <td>
                  1.0.0
                      </td>
          </tr>
          <tr>
              <td>
                  <b>Created</b>
              </td>
              <td>
                  2025-12-15
                      </td>
          </tr>
          <tr>
              <td>
                  <b>Description</b>
              </td>
              <td>
                  Microservices-based e-commerce platform for order processing, inventory management, and payments
                      </td>
          </tr>
          <tr>
              <td>
                  <b>Tags</b>
              </td>
              <td>
                  <ul>
                      <li>ecommerce</li>
                      <li>microservices</li>
                      <li>orders</li>
                  </ul>
              </td>
          </tr>
          </tbody>
      </table>
  </div>

## Adrs
- [docs/adr/0001-use-message-queue-for-async-processing.md](docs/adr/0001-use-message-queue-for-async-processing.md)
- [docs/adr/0002-use-oauth2-for-api-authentication.md](docs/adr/0002-use-oauth2-for-api-authentication.md)
