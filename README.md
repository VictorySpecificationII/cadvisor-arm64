# cadvisor-arm64
Dockerfile for cadvisor for the arm64 architecture

## Use

- docker build -t cadvisor-arm64 .
- docker run -d -p 8080:8080 cadvisor-arm64:latest

In your prometheus.yml file, add:

```
  - job_name: 'cadvisor'
    static_configs:
      - targets: ['machineip:8080']

```
