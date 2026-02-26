# OSINT Project: Attack Surface Mapping of VulnWeb

## 🎯 Overview
This project demonstrates an automated reconnaissance exercise conducted against `vulnweb.com`. As a senior cybersecurity student, I used this to practice mapping organizational infrastructure and identifying technology stacks using passive OSINT techniques.

## 🛠 Methodology
- **Tools:** SpiderFoot (running in a dedicated Python 3.11 Conda environment on macOS).
- **Techniques:** Recursive DNS brute-forcing, web metadata extraction, and service banner grabbing.
- **Approach:** Strictly passive to ensure zero-impact on target availability.

## 📊 Infrastructure Visualization
![Network Map](./graph_visualization.png)
*Relationship map showing DNS authority, Mail servers, and discovered subdomains.*

## 🔍 Key Findings
- **Subdomain Enumeration:** Identified `testaspnet`, `testasp`, and `testhtml5` subdomains.
- **Technology Fingerprinting:** Target is utilizing **Nginx 1.19.0**, **ASP.NET**, and **AngularJS**.
- **Email/DNS Logic:** Mapped 5 Google MX records and Gandi.net name servers.
- * **DNS Misconfiguration Identification:** Discovered `localhost.vulnweb.com`. Identifying internal-facing naming conventions in public DNS records is a high-value OSINT finding, as it suggests potential leaks from development or internal environments that could be leveraged for further exploitation.

## 📂 Project Artifacts
- `recon_results.csv`: Full intelligence dataset.
- `network_graph.gexf`: Graph data for advanced visualization.
