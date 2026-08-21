_MLOps Syllabus — Deploy and Retrain ML Models on AWS_

## Quick Start

```bash
pip install -r requirements.txt
cd src && python generate_data.py
python train.py && cd ..
streamlit run src/app.py
```

## Run with Docker

```bash
docker build -t fraud-detection-app:v1.0 .
docker run -p 8501:8501 fraud-detection-app:v1.0
```

Open browser → http://localhost:8501

## Project Structure

```
fraud-detection/
├── src/
│   ├── generate_data.py   → creates sample data
│   ├── preprocess.py      → feature engineering
│   ├── train.py           → trains model
│   ├── predict.py         → makes predictions
│   └── app.py             → Streamlit frontend
├── tests/
│   └── test_model.py      → 8 pytest tests
├── models/                → saved model (gitignored)
├── data/                  → transaction data (gitignored)
├── Dockerfile             → Docker build instructions
├── .dockerignore          → files excluded from Docker
├── .gitignore             → files excluded from Git
└── requirements.txt       → all libraries
```
