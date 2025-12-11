# Sentiment Analysis MLOps Pipeline

This is an end-to-end MLOps project that implements a Sentiment Analysis pipeline using Flask, DVC, and MLflow.

## 🚀 Getting Started

### Prerequisites
*   Python 3.10+
*   Docker (optional, for containerization)
*   Git

### ⚙️ Configuration
Before running the project, you **must** configure the following settings:

1.  **Data Source**:
    *   Open `src/data/data_ingestion.py`.
    *   Update `data_url` with a valid URL to your CSV dataset.

2.  **MLflow / DagsHub**:
    *   Open `flask_app/app.py` and `src/model/register_model.py`.
    *   Update `repo_owner` with your DagsHub username.
    *   Ensure you have the required environment variables set (e.g., `MLFLOW_TRACKING_USERNAME`, `MLFLOW_TRACKING_PASSWORD`).

### 📦 Installation

```bash
pip install -r requirements.txt
```

### 🏃 Setup & Run Pipeline

This project uses DVC to manage the pipeline phases.

```bash
# Run the entire pipeline
dvc repro
```

### 🌐 Run Web App

```bash
cd flask_app
python app.py
```

### 🐳 Run with Docker

```bash
docker build -t sentiment-app .
docker run -p 5000:5000 sentiment-app
```
