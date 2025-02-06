# ETL Sales Data Pipeline 🚀

## 📌 Project Overview
This project automates an ETL pipeline that extracts customer sales data from an API and an SQL database, transforms it, and loads it into a PostgreSQL data warehouse. The process is scheduled and monitored using Apache Airflow.

## 📌 Features
✅ Extracts data from an API and a PostgreSQL database  
✅ Cleans & transforms data (handling nulls, duplicates, aggregations)  
✅ Loads processed data into a PostgreSQL database  
✅ Automates the ETL process using Apache Airflow  
✅ Implements unit testing for validation  
✅ Deployable via Docker for scalability  

---

## 📌 Project Structure
```
etl-sales-pipeline/
│── data/                          # Sample or raw data (ignored in production)
│   ├── sample_api_data.json
│   ├── sample_sql_data.csv
│
│── dags/                          # Airflow DAGs for scheduling the ETL pipeline
│   ├── etl_pipeline.py            # Main DAG definition
│
│── scripts/                       # Python scripts for each ETL step
│   ├── extract.py                 # Extract data from API & SQL
│   ├── transform.py               # Data cleaning & transformation
│   ├── load.py                    # Load transformed data into DB
│
│── config/                        # Configuration files for database & API access
│   ├── db_config.yaml             # Database connection settings
│   ├── api_config.yaml            # API keys & endpoints
│
│── notebooks/                     # Jupyter notebooks for testing
│   ├── etl_pipeline_test.ipynb    # Interactive notebook for debugging ETL
│
│── tests/                         # Unit tests for ETL scripts
│   ├── test_extract.py            # Test extraction functions
│   ├── test_transform.py          # Test transformation functions
│   ├── test_load.py               # Test data loading functions
│
│── logs/                          # Logs directory (ignored in .gitignore)
│
│── .gitignore                      # Ignore unnecessary files (logs, env, data)
│── requirements.txt                # Required Python libraries
│── README.md                       # Project documentation
│── docker-compose.yml              # Docker setup (optional)
│── airflow.cfg                      # Airflow configuration (if using Airflow)
```

---

## 📌 Installation & Setup

### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/yourusername/etl-sales-pipeline.git
cd etl-sales-pipeline
```

### **2️⃣ Install Dependencies**
```bash
pip install -r requirements.txt
```

### **3️⃣ Set Up PostgreSQL Database**
Create a PostgreSQL database and configure `config/db_config.yaml` with your credentials.

### **4️⃣ Run ETL Pipeline**
Execute each script sequentially:
```bash
python scripts/extract.py
python scripts/transform.py
python scripts/load.py
```

### **5️⃣ (Optional) Set Up Airflow for Automation**
```bash
airflow db init
airflow scheduler &
airflow webserver &
```

---

## 📌 Technologies Used
- **Python** (ETL scripting)
- **Pandas & SQLAlchemy** (Data processing)
- **PostgreSQL** (Data warehouse)
- **Apache Airflow** (Automation)
- **Docker** (Deployment)

---

## 📌 License
This project is licensed under the MIT License.

---

### **🚀 Future Enhancements**
✅ Implement logging & monitoring using Prometheus & Grafana  
✅ Improve error handling & exception logging  
✅ Deploy the pipeline to cloud platforms (AWS, GCP)  

Would you like a sample dataset for testing? 😊

