# **ISP Infrastructure Deployment**  

## **Project Overview**  
This project focuses on deploying **infrastructure services for an Internet Service Provider (ISP)** using a **GPON network** in the i2t lab. The implementation includes the installation and evaluation of **LibreQoS** ([libreqos.io](https://libreqos.io/)) to analyze network performance, with the possibility of extending the deployment to a real ISP environment.  

Additionally, the network will incorporate a **wireless communication component based on TV White Spaces (TVWS)**, which may require multiple **VLANs** to ensure efficient traffic segmentation.  

## **Core Infrastructure Services**  
The project aims to establish the essential network services required for ISP operations, including:  
- **DHCP Server** for dynamic IP allocation.  
- **Web Server** (preferably supporting **QUIC** for enhanced performance).  
- **DNS Server** for domain name resolution.  
- **Virtualized Services**:  
  - **Firewall** for network security.  
  - **Load Balancer** to optimize traffic distribution.  

Additionally, **OSM (Open Source MANO)** ([osm.etsi.org](https://osm.etsi.org/)) may be explored as an optional component for network service orchestration.  

## **Project Milestones**  
The implementation is structured into the following key phases:  

### **1️⃣ Deployment of a Virtual Infrastructure Manager (VIM)**  
The platform will be deployed using either:  
- **Red Hat OpenStack Platform (RHOSP)** or  
- **VMware**  

### **2️⃣ Kubernetes (K8s) and Grafana Integration**  
- **Kubernetes** will be utilized for container orchestration.  
- **Grafana (with Prometheus)** will provide real-time monitoring and analytics.  

### **3️⃣ Network Management Tools**  
- Deployment of a **network management solution** such as **Zabbix** or **OpenWISP** for monitoring and administration.  

## **Infrastructure & Deployment**  
The system will be deployed on **one or more virtual machines**, running:  
- **Linux** as the base operating system.  
- **Kubernetes (K8s)** for service containerization.  
- **Grafana** for visualization and monitoring.  

The development timeline includes scheduled milestones, with the initial phase focusing on infrastructure setup and validation.  
