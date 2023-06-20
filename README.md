# grafana-dashboards

Grafana dashboards for Crowdsec monitoring using Prometheus

 - `./dashboards_v4` are compatible with releases `v1.4.X`

 - `./dashboards_v5` are compatible with releases `v1.5.X` (tested with Grafana 10.0 and Grafana cloud)

![](https://doc.crowdsec.net/Crowdsec/v0/assets/images/grafana_overview.png)

![](https://doc.crowdsec.net/Crowdsec/v0/assets/images/grafana_insight.png)

![](https://doc.crowdsec.net/Crowdsec/v0/assets/images/grafana_details.png) 


## Legacy dashboards

 - `./dashboards_v1` are compatible for releases `v0.3.0-rc0` and below.

 - `./dashboards_v2` are compatible for releases `v0.3.0-rc1`, up to `v1.0.X`.

 - `./dashboards_v3` are compatible for releases `v1.1.X` and up.

## Prometheus config (for v4 and earlier versions)

For dashboards v4 and earlier, label is used to filter on individual machines. It's recommended to follow this config example:

```yaml
  - job_name: 'crowdsec_myMachine'
    static_configs:
    - targets: ['1.2.3.4:6060']
      labels:
        machine: 'my_machine'
```
