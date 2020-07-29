### Todo app (dotnet core) with monitoring using prometheus client library.

#### TODO App
https://docs.microsoft.com/en-us/aspnet/core/tutorials/first-web-api?view=aspnetcore-3.1&tabs=visual-studio

#### Prometheus Client Library
https://github.com/prometheus-net/prometheus-net

#### Prometheus Client Libraries
https://prometheus.io/docs/instrumenting/clientlibs/


#### Prometheus scrape config

```yml
  - job_name: 'dotnet-core-todo'
    # scrape_interval: 15s
    metrics_path: /metrics
    scheme: https
    tls_config:
      insecure_skip_verify: true
    static_configs:
      - targets: ['localhost:5001']
```
