# grafana-dashboards
Grafana dashboards for Crowdsec monitoring using Prometheus


`./dashboards_v1` are compatible for releases `v0.3.0-rc0` and below.

`./dashboards_v2` are compatible for releases `v0.3.0-rc1`, up to `v1.0.X`.

`./dashboards_v3` are compatible for releases `v1.1.X` and up.

`./dashboards_v4` are compatible for releases `v1.4.X` and up.


![](https://doc.crowdsec.net/Crowdsec/v0/assets/images/grafana_overview.png)

![](https://doc.crowdsec.net/Crowdsec/v0/assets/images/grafana_insight.png)

![](https://doc.crowdsec.net/Crowdsec/v0/assets/images/grafana_details.png) 

## Prometheus config
The dashboards use label to filter on individual machines. It's recommended to follow this config example:

```yaml
  - job_name: 'crowdsec_myMachine'
    static_configs:
    - targets: ['1.2.3.4:6060']
      labels:
        machine: 'my_machine'
```
