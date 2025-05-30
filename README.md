# 🍺 Beer Project: Graph Database Analysis of Beers and Breweries

This project utilizes a graph database approach to analyze relationships between beers, breweries, and related attributes. By modeling the data as a graph, we can uncover insights into the beer industry, such as identifying popular beer styles, exploring brewery collaborations, and understanding regional beer distributions.

## 📁 Repository Contents

- `BDMM_HOMEWORK_1_Final_2024.ipynb`: Jupyter Notebook containing the data modeling, analysis, and visualization of the beer and brewery graph.
- `README.md`: Project documentation.

## 🛠️ Technologies & Tools

- **Programming Language**: Python
- **Graph Database**: Neo4j (via Docker container)
- **Containerization**: Docker
- **Libraries**:
  - Data Handling: `pandas`
  - Graph Analysis: `networkx`
  - Visualization: `matplotlib`, `seaborn`
- **Environment**: Jupyter Notebook

## 🔍 Analysis Overview

The analysis includes:

- **Data Modeling**: Representing beers, breweries, and their relationships as nodes and edges in a graph.
- **Exploratory Data Analysis (EDA)**: Investigating the properties of the graph, such as node degrees, centrality measures, and community structures.
- **Visualization**: Creating visual representations of the graph to identify patterns and clusters.
- **Insights**: Deriving meaningful conclusions about the beer industry based on the graph analysis.

## 🚀 Getting Started

### Prerequisites

- Python 3.8 or higher
- Jupyter Notebook
- Docker
- Neo4j Docker image

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/dcavaleiro/Beer_project.git
   cd Beer_project

## 🧱 Neo4j Database Setup

To explore the graph database and run the analysis, follow these steps to set up your Neo4j instance using Docker.

### 🔄 Stop Existing Containers

Ensure that no existing Neo4j containers are running:

- Using Docker Desktop: Stop the `Neo4JLab` container.
- Or via command line:
  ```bash
  docker stop Neo4JLab

## 🐳 Launch Docker Container
Replace the paths in the command below with the correct paths on your system:
```bash
docker run --name Neo4JHW -p 7474:7474 -p 7687:7687 -d ^
-v "C:\Path\To\Neo4JPlugins":/plugins ^
-v "C:\Path\To\Neo4JHWData\data":/data ^
--env NEO4J_AUTH=neo4j/test ^
--env NEO4J_dbms_connector_https_advertised__address="localhost:7473" ^
--env NEO4J_dbms_connector_http_advertised__address="localhost:7474" ^
--env NEO4J_dbms_connector_bolt_advertised__address="localhost:7687" ^
--env NEO4J_dbms_security_procedures_unrestricted="gds.*" ^
--env NEO4J_dbms_security_procedures_allowlist="gds.*" ^
neo4j:4.4.5

