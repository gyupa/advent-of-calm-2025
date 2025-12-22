---
id: order-service-connects-order-database
title: Order Service Connects Order Database
---

## Details
<div className="table-container">
| Field               | Value                    |
|---------------------|--------------------------|
| **Unique ID**       | order-service-connects-order-database                   |
| **Description**      |  Order Service reads and writes order data to the Order Database   |
</div>

## Related Nodes
```mermaid
graph TD;
order-service -- Connects --> order-database;

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
                  &lt; 100ms
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
                  false
                      </td>
          </tr>
          </tbody>
      </table>
  </div>
