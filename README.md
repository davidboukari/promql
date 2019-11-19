# promql
In prometheus.yml it is possible to add any label ex: product, env, 
```bash
...
...
- job_name: 'promotheus1-node1'
    static_configs:
      - targets: ['192.168.85.20:9100']
        labels:
          product: 'myproduct1'
          env: 'prd'

```
## Queries: Promql, prometheus, Grafana ##

* node_load1
* node_load1{instance="192.168.85.20:9100",job="promotheus1-node1"}
* node_load1{instance="192.168.85.30:9100",job="consul",service="node_exporter"}
* node_load1{job=~".+"}
* node_load1{job=~"consul.+"}
* node_load1{job=~"consul.*"} or node_load1{instance=~"192.*"} 
* node_load1{instance=~"192.*", product=~"my.+"} 
* node_load1{env=~"prd"}
