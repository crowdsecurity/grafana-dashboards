# grafana-dashboards
Grafana dashboards for Crowdsec monitoring using Prometheus


`./dashboards_v1` are compatible for releases `v0.3.0-rc0` and below

`./dashboards_v2` are compatible for releases `v0.3.0-rc1` and up 


## Prometheus config
The dashboards use label to filter on individual machines. It's recommended to follow this config example:

```yaml
  - job_name: 'crowdsec_myMachine'
    static_configs:
    - targets: ['1.2.3.4:6060']
      labels:
        machine: 'my_machine'
```
