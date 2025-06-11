# **ISP Infrastructure Deployment**  

## **Project Overview**  
This project focuses on deploying **infrastructure services for an Internet Service Provider (ISP)** using a **GPON network** in the i2t lab. The implementation includes the installation and evaluation of **LibreQoS** ([libreqos.io](https://libreqos.io/)) to analyze network performance, with the possibility of extending the deployment to a real ISP environment.  

Additionally, the network will incorporate a **wireless communication component based on TV White Spaces (TVWS)**, which may require multiple **VLANs** to ensure efficient traffic segmentation.  

 # Logical and physical network diagram: 

[![Figma Design for diagrams](path/to/your/image.png)](https://www.figma.com/design/i5gnODzQy96CFGwsyb3TJU/Untitled?node-id=0-1&t=un5PoFwpIqhN0i5b-1)

---

## ISP Infrastructure Deployment Achievements

We successfully built a robust ISP infrastructure in the i2t lab, integrating a **GPON network** with a **TV White Spaces (TVWS)** wireless component. Here's a rundown of what we achieved:

* **DHCP (Dynamic Host Configuration Protocol):** We implemented **KEA DHCP** for automatic IP address assignment. While we couldn't configure DHCP relay on the Huawei OLT, KEA handles IP distribution for other essential network segments, ensuring seamless connectivity for our equipment.

* **DNS (Domain Name System):** Our **DNS server** was set up using **BIND**. It's a private DNS instance and, due to NAT and network restrictions at ICESI, it couldn't connect with external authoritative DNS servers. However, it effectively manages internal domain name resolution.

* **Iperf:** **Iperf** is fully integrated, providing a crucial tool for network performance measurement. This allows us to test and validate bandwidth, latency, and jitter across both the GPON and TVWS segments.

* **Webservers:** We deployed multiple **web servers** that utilize **QUIC with HTTP/3.0** for efficient and secure content delivery. These servers are ready to host web-based applications or content, vital for internal management tools or basic customer-facing services.

* **Load Balancer:** A **load balancer** was implemented to distribute incoming network traffic across our web servers. This setup enhances service availability, improves response times, and ensures efficient resource utilization.

* **Firewall:** Network security is managed through **Access Control Lists (ACLs)**, which we configured directly on the final router. These ACLs control traffic flow based on predefined security rules, protecting our ISP infrastructure and data.

* **LibreQoS:** **LibreQoS ([libreqos.io](https://libreqos.io/))** is successfully installed and operational, enabling advanced Quality of Service (QoS) management across the network. This was crucial for intelligent bandwidth allocation and traffic prioritization, helping us deliver a consistent user experience.

* **Grafana + Prometheus:** We integrated **Grafana and Prometheus** for comprehensive monitoring of our two main servers. Prometheus collects key metrics, while Grafana provides intuitive dashboards to display real-time performance data and alerts from these servers.

* **FreeRADIUS:** Although planned for authentication, authorization, and accounting (AAA) services, **FreeRADIUS** could not be fully integrated due to the absence of PPPoE relay capabilities in our setup.

* **TVWS (Master-Slave):** The **TV White Spaces (TVWS) wireless communication component** was successfully deployed in a master-slave configuration, effectively extending network reach and providing alternative connectivity options.

* **LibreNMS:** **LibreNMS** is integrated as an auto-discovering network monitoring system. It provides a comprehensive overview of **all network devices**, continuously tracking their status and performance metrics.

* **Dual Stack:** Our network supports **Dual Stack (IPv4 and IPv6)**. For IPv6, we utilized **SLAAC (Stateless Address Autoconfiguration)**, assigning addresses using documentation IPs, ensuring compatibility with modern internet standards in our lab environment.

* **QoS Plans:** We established custom **QoS plans** that work in conjunction with LibreQoS. These plans prioritize different types of traffic—such as streaming, video, and web data—to guarantee specific service levels for various customer tiers.

![image](https://github.com/user-attachments/assets/1b532624-cb77-4869-82bc-1b6058287182)


