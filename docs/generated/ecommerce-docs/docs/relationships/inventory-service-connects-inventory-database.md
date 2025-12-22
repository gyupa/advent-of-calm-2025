---
id: inventory-service-connects-inventory-database
title: Inventory Service Connects Inventory Database
---

## Details
<div className="table-container">
| Field               | Value                    |
|---------------------|--------------------------|
| **Unique ID**       | inventory-service-connects-inventory-database                   |
| **Description**      |  Inventory Service reads and writes inventory data to the Inventory Database   |
</div>

## Related Nodes
```mermaid
graph TD;
inventory-service -- Connects --> inventory-database;

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
