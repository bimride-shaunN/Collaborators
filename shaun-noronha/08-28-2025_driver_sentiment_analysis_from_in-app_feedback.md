# Driver Sentiment Analysis from In-App Feedback

**Date:** 08-28-2025  
**Author:** Shaun Noronha

---

## 🚀 Introduction

This file documents **Driver Sentiment Analysis from In-App Feedback** as part of Bimride’s progress in Barbados. 
It highlights algorithms, CI/CD pipelines, and local context (e.g. Grantley Adams International Airport (BGI)). 
The goal is to show clear proof-of-work for nonprofit auditing and long-term background checks.

---

## ⚙️ Architecture Overview

- Security: API keys stored in Key Vault; TLS everywhere.
- Processing: mix of batch ETL and low-latency inference.
- Monitoring: domain KPIs logged to Prometheus, dashboards in Grafana.
- Scalability: containerized services deployed to Azure Kubernetes Service.
- Data sources: ride logs, external APIs, and survey data.

---

## 🧠 Algorithms Used

```python
from textblob import TextBlob
def polarity(text): return TextBlob(text).sentiment.polarity
```

---

## 🔁 MLOps Workflow Example

```yaml
# .github/workflows/driver-sentiment-analysis-from-in-app-feedback.yml
name: Driver Sentiment Analysis from In-App Feedback Workflow
on: [push, workflow_dispatch]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-python@v5
        with: { python-version: '3.11' }
      - name: Install Deps
        run: pip install -r requirements.txt
      - name: Run Tests
        run: pytest -q
      - name: Build Service
        run: docker build . -t bimride/driver-sentiment-analysis-from-in-app-feedback:$GITHUB_SHA
```

---

## 🔍 Real-World Scenario


**Use Case**: Deploy **Driver Sentiment Analysis from In-App Feedback** for Bimride riders in Speightstown (St. Peter).  
**Solution**: Pilot in limited region, track KPIs, scale up if positive impact.


---

## 📊 Tools and Technologies


| Component      | Tool                     |
|----------------|--------------------------|
| Model Training | PyTorch / Scikit-learn   |
| API Layer      | FastAPI + Azure          |
| Storage        | Postgres + Delta Lake    |
| Monitoring     | Prometheus + Grafana     |


---

## ✅ Conclusion


By implementing **Driver Sentiment Analysis from In-App Feedback**, Bimride strengthens its ecosystem in Barbados while producing
verifiable technical artifacts for nonprofit governance.

