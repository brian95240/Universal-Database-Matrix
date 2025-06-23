# Universal Database Matrix

[![Deploy](https://github.com/your-username/Universal-Database-Matrix/actions/workflows/deploy.yml/badge.svg)](https://github.com/your-username/Universal-Database-Matrix/actions/workflows/deploy.yml)

The Universal Database Matrix is a complete, enterprise-grade FOSS database and graph analytics platform designed for maximum efficiency and accessibility. [span_0](start_span)[span_1](start_span)It transforms complex data operations into an intuitive, conversational experience through a unique Windows XP-inspired interface.[span_0](end_span)[span_1](end_span)

[span_2](start_span)The entire stack is packaged for a one-command deployment on Hetzner Cloud,[span_2](end_span) [span_3](start_span)[span_4](start_span)delivering a production-ready environment in under 10 minutes for a fraction of the cost of major cloud providers.[span_3](end_span)[span_4](end_span)

## ✨ Key Features

* **[span_5](start_span)Complete FOSS Stack**: Integrates a full suite of powerful tools including PostgreSQL, Apache AGE for graph queries, PostGIS, MADlib for in-database machine learning, and NetworkX.[span_5](end_span)
* **[span_6](start_span)[span_7](start_span)One-Command Deployment**: A single shell script provisions the Hetzner Cloud infrastructure, installs K3s, and deploys the entire application stack.[span_6](end_span)[span_7](end_span)
* **[span_8](start_span)Extreme Cost-Efficiency**: Run a full production-grade setup on Hetzner Cloud for approximately **€16.46/month**, an 88-94% cost reduction compared to equivalent setups on AWS, Azure, or GCP.[span_8](end_span)
* **[span_9](start_span)[span_10](start_span)Windows XP-Inspired UI**: A familiar dual-layer interface that allows users to seamlessly toggle between a traditional Database Layer and a visual Graph Layer.[span_9](end_span)[span_10](end_span)
* **[span_11](start_span)[span_12](start_span)[span_13](start_span)[span_14](start_span)Intelligent Configuration**: A web-based configuration management interface with a wizard to simplify editing settings for KEDA, Prometheus, Grafana, and other tools.[span_11](end_span)[span_12](end_span)[span_13](end_span)[span_14](end_span)
* **[span_15](start_span)[span_16](start_span)Automated Resource Scaling**: Pre-configured KEDA auto-scaling responds to application load, scaling resources up and down to ensure performance and cost-efficiency.[span_15](end_span)[span_16](end_span)
* **[span_17](start_span)[span_18](start_span)Built-in Orchestration & Monitoring**: Leverages Prefect for complex, cascading workflow automation[span_17](end_span)[span_18](end_span) [span_19](start_span)and a Prometheus/Grafana stack for comprehensive, real-time monitoring.[span_19](end_span)

## 🏗️ Architecture

[span_20](start_span)The system runs a multi-pod architecture on a lightweight K3s cluster.[span_20](end_span) This separates concerns, allowing components to be managed and scaled independently.

* **[span_21](start_span)Deployment**: Single-command deployment script using pre-configured Kubernetes manifests.[span_21](end_span)
* **[span_22](start_span)[span_23](start_span)UI Layer**: A Node.js application serves the Windows XP-style interface with its dual-layer toggle system.[span_22](end_span)[span_23](end_span)
* **[span_24](start_span)[span_25](start_span)Data Layer**: A stateful set runs a Hetzner-optimized instance of PostgreSQL with the Apache AGE extension enabled, using persistent volumes for storage.[span_24](end_span)[span_25](end_span)
* **[span_26](start_span)[span_27](start_span)Automation & Scaling**: KEDA and Prefect run as separate deployments, interacting with the main application and database based on pre-defined workflows and scaling triggers.[span_26](end_span)[span_27](end_span)

## 🚀 Getting Started: 5-Minute Deployment

### Prerequisites

1.  A **Hetzner Cloud** account.
2.  Your **Hetzner Cloud API Token**.

### Deployment

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/Universal-Database-Matrix.git](https://github.com/your-username/Universal-Database-Matrix.git)
    cd Universal-Database-Matrix
    ```

2.  **Set your Hetzner API Token:**
    ```bash
    export HCLOUD_TOKEN="your-hetzner-cloud-token"
    ```

3.  **Run the deployment script:**
    ```bash
    ./deploy-hetzner.sh
    ```
    The script will create the server, install K3s, and deploy all application components. [span_28](start_span)This process typically takes 5-10 minutes.[span_28](end_span)

4.  **Access Your System:**
    [span_29](start_span)[span_30](start_span)At the end of the script, the access URL will be displayed.[span_29](end_span)[span_30](end_span)

## 🔧 Configuration

Initial configuration is handled automatically by the deployment script. For ongoing management:

* **[span_31](start_span)[span_32](start_span)Easy Mode**: Use the integrated **Configuration Management** web interface to edit configs with a wizard.[span_31](end_span)[span_32](end_span)
* **[span_33](start_span)Advanced Mode**: Modify the YAML and configuration files in the `config/` and `manifests/` directories and redeploy by pushing to your `main` branch (if CI/CD is configured).[span_33](end_span)

## 🛠️ Technology Stack

| Category                  | Technology                                                     |
| ------------------------- | -------------------------------------------------------------- |
| **Cloud & Orchestration** | Hetzner Cloud, K3s, KEDA                                       |
| **Database** | Neon PostgreSQL, Apache AGE, PostGIS                           |
| **Analytics & ML** | MADlib, NetworkX                                               |
| **Workflow Automation** | Prefect                                                        |
| **Monitoring** | Prometheus, Grafana                                            |
| **Backend** | Node.js (Express)                                              |
| **Frontend** | Custom Windows XP UI, D3.js/Cytoscape                          |

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for details.
