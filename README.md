# AWS Production Monitoring

A simple AWS monitoring project using Prometheus, Grafana, and Node Exporter.

## Architecture

```text
AWS EC2
   |
 Docker
   |
 +-----------------------+
 | Prometheus            |
 | Grafana               |
 | Node Exporter         |
 +-----------------------+
```

## Tools Used

* AWS EC2
* Ubuntu
* Docker
* Docker Compose
* Prometheus
* Grafana
* Node Exporter
* GitHub

## What I Did

* Created an AWS EC2 server.
* Installed Docker and Docker Compose.
* Deployed Prometheus, Grafana, and Node Exporter.
* Configured Prometheus to collect server metrics.
* Connected Grafana with Prometheus.
* Created monitoring dashboards.
* Monitored CPU, memory, disk, and network.
* Stored the project in GitHub.
* Tested deploying the project on another EC2 server.

## Project Structure

```text
aws-production-monitoring/
├── docker-compose.yml
├── prometheus/
│   └── prometheus.yml
└── README.md
```

## Run

```bash
git clone https://github.com/Rithick-18/aws-production-monitoring.git
cd aws-production-monitoring
docker compose up -d
```

Check containers:

```bash
docker ps
```

## Access

Prometheus:

```text
http://<EC2-IP>:9090
```

Grafana:

```text
http://<EC2-IP>:3000
```

## Alert Testing

CloudWatch CPU alarm and SNS email notification were also tested successfully.

```text
EC2 → CloudWatch → Alarm → SNS → Email
```

The test successfully triggered an alert when CPU crossed **80%**.

CloudWatch and SNS resources were deleted after testing to avoid unnecessary cost.

## Status

* ✅ EC2
* ✅ Docker
* ✅ Prometheus
* ✅ Grafana
* ✅ Node Exporter
* ✅ GitHub
* ✅ CloudWatch Alert Testing
* ✅ SNS Email Testing

