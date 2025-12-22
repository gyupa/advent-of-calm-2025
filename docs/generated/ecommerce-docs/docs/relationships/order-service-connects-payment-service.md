---
id: order-service-connects-payment-service
title: Order Service Connects Payment Service
---

## Details
<div className="table-container">
| Field               | Value                    |
|---------------------|--------------------------|
| **Unique ID**       | order-service-connects-payment-service                   |
| **Description**      |  Order Service initiates payments with Payment Service   |
</div>

## Related Nodes
```mermaid
graph TD;
order-service -- Connects --> payment-service;

```

## Controls
    _No controls defined._

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
                  <b>Latency Sla</b>
              </td>
              <td>
                  &lt; 1000ms
                      </td>
          </tr>
          <tr>
              <td>
                  <b>Monitoring</b>
              </td>
              <td>
                  true
                      </td>
          </tr>
          <tr>
              <td>
                  <b>Circuit Breaker</b>
              </td>
              <td>
                  true
                      </td>
          </tr>
          </tbody>
      </table>
  </div>
