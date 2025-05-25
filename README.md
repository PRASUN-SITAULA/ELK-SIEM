# ELK-SIEM: Security Information and Event Management

A comprehensive ELK (Elasticsearch, Logstash, Kibana) stack implementation for Security Information and Event Management (SIEM), specifically designed for analyzing Kali Linux security logs.

## Project Overview

This project demonstrates the implementation of a simple SIEM solution using the ELK stack to collect, process, analyze, and visualize security logs from Kali Linux system VM. The setup provides real-time monitoring capabilities for security events.

## Architecture

```
┌─────────────┐    ┌──────────────┐    ┌─────────────────┐    ┌─────────────┐
│ Kali Linux  │───▶│   Logstash   │───▶│ Elasticsearch   │───▶│   Kibana    │
│   (filbeat) │    │ (Processing) │    │   (Storage)     │    │(Visualization)│
└─────────────┘    └──────────────┘    └─────────────────┘    └─────────────┘
```


## Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/PRASUN-SITAULA/ELK-SIEM.git
cd ELK-SIEM
```

### 2. Start ELK Stack
```bash
# Start all services
docker-compose up -d

# Verify services are running
docker-compose ps
```
### 3.Start Filebeat
```bash
# Start filebeat
docker-compose up -d filebeat
```

### 4. Access Services
- **Kibana**: http://localhost:5601
- **Elasticsearch**: http://localhost:9200
- **Logstash**: http://localhost:5000 (for log inputs)


## 🔐 Security Considerations

- Change default passwords for all services
- Enable authentication for Elasticsearch and Kibana
- Configure SSL/TLS encryption
- Implement proper network segmentation
- Regular backup of indices
- Monitor disk space usage

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
