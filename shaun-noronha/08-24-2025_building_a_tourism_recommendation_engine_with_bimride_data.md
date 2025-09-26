# Building a Tourism Recommendation Engine with Bimride Data

**Date:** 08-24-2025  
**Author:** Shaun Noronha

---

## 🚀 Introduction

This file documents **Building a Tourism Recommendation Engine with Bimride Data** as part of Bimride’s progress in Barbados. 
It highlights algorithms, CI/CD pipelines, and local context (e.g. Speightstown (St. Peter)). 
The goal is to show clear proof-of-work for nonprofit auditing and long-term background checks.

---

## ⚙️ Architecture Overview

- Security: API keys stored in Key Vault; TLS everywhere.
- Processing: mix of batch ETL and low-latency inference.
- Data sources: ride logs, external APIs, and survey data.
- Scalability: containerized services deployed to Azure Kubernetes Service.
- Monitoring: domain KPIs logged to Prometheus, dashboards in Grafana.

---

## 🧠 Algorithms Used

```python
import numpy as np
def recommend(user_vec, item_mat):
    scores = item_mat @ user_vec
    return np.argsort(-scores)[:5]
```

---

## 🔁 MLOps Workflow Example

```yaml
# .github/workflows/building-a-tourism-recommendation-engine-with-bimride-data.yml
name: Building a Tourism Recommendation Engine with Bimride Data Workflow
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
        run: docker build . -t bimride/building-a-tourism-recommendation-engine-with-bimride-data:$GITHUB_SHA
```

---

## 🔍 Real-World Scenario


**Use Case**: Deploy **Building a Tourism Recommendation Engine with Bimride Data** for Bimride riders in Grantley Adams International Airport (BGI).  
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


By implementing **Building a Tourism Recommendation Engine with Bimride Data**, Bimride strengthens its ecosystem in Barbados while producing
verifiable technical artifacts for nonprofit governance.

