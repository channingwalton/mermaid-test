# mermaid-test
test the chrome mermaid plugin

```mermaid
flowchart LR
  RokuUI["A"]-- transaction --> troute["route"]
  B-- push notification --> proute["route"]
  troute -- id -->handlerIn["accept"]
  proute -- notification -->handlerIn
  subgraph Handler
    handlerIn -- json --> idb[(Database)]
    handlerIn -- action --> process[process]
    process -- refine --> handlerIn
    process -- email --> user
    process -- event --> store
  end
```
