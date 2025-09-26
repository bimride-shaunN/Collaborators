# Building a Tourism Recommendation Engine with Bimride Data

**Date:** 08-24-2025  
**Author:** Shaun Noronha  

---

## 🚀 Introduction  

Tourism is the backbone of Barbados’s economy, and Bimride plays a vital role in moving visitors between attractions.  
Currently, riders search manually for destinations. A **Tourism Recommendation Engine** can improve user experience by:  

- Suggesting personalized destinations based on ride history.  
- Promoting local businesses fairly.  
- Reducing rider indecision, especially for first-time tourists.  

This project leverages **machine learning recommendation systems** to make Bimride not just a transport service, but a **travel guide for Barbados**.  

---

## ⚙️ Architecture Overview  

The recommendation pipeline is designed as follows:  

```
        +-------------------+
        | Ride History Data |
        +-------------------+
                 |
                 v
        +-------------------+
        |   Feature Store   |  <-- Trip frequency, POI categories
        +-------------------+
                 |
                 v
        +-------------------+       +----------------------+
        | Recommender Model | <---> | Tourism POI Database |
        +-------------------+       +----------------------+
                 |
                 v
        +-------------------+
        |   Rider App API   |
        +-------------------+
```

Key components:  
- **Ride History Data**: Pickups/drop-offs, timestamps.  
- **Tourism POI Database**: Museums, beaches, restaurants.  
- **Model**: Collaborative filtering + embeddings.  
- **Delivery**: Suggestions appear when a rider opens the app.  

---

## 🧠 Algorithms Used  

### Matrix Factorization for Tourism Recommendations  

```python
import numpy as np

# Example: 3 users x 4 destinations matrix (ratings/frequency)
R = np.array([
    [5, 3, 0, 1],
    [4, 0, 0, 1],
    [1, 1, 0, 5]
])

# Matrix factorization with SGD
num_users, num_items = R.shape
K = 2  # latent dimensions

P = np.random.rand(num_users, K)
Q = np.random.rand(num_items, K)

alpha, beta = 0.01, 0.02

for epoch in range(1000):
    for i in range(num_users):
        for j in range(num_items):
            if R[i, j] > 0:
                eij = R[i, j] - np.dot(P[i, :], Q[j, :].T)
                for k in range(K):
                    P[i, k] += alpha * (2 * eij * Q[j, k] - beta * P[i, k])
                    Q[j, k] += alpha * (2 * eij * P[i, k] - beta * Q[j, k])

print("Recommendation scores:\n", np.dot(P, Q.T))
```

---

## 🔁 MLOps Workflow Example  

```yaml
# .github/workflows/train-tourism-recommender.yml
name: Tourism Recommender Training

on:
  schedule:
    - cron: "0 2 * * 1"  # Train every Monday
  workflow_dispatch:

jobs:
  train:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Set up Python
        uses: actions/setup-python@v5
        with:
          python-version: "3.11"
      - name: Install dependencies
        run: pip install -r requirements.txt
      - name: Run training script
        run: python train_recommender.py --epochs 20 --embedding_dim 64
      - name: Evaluate model
        run: python evaluate_recommender.py
      - name: Push model to Azure Blob
        run: az storage blob upload --file models/recommender.pkl --container ml-models
```

---

## 🔍 Real-World Scenario  

During **Crop Over Festival** in Bridgetown, thousands of tourists use Bimride to explore the island.  

- A visitor from the cruise terminal books a ride to Carlisle Bay.  
- The recommender, recognizing interest in beaches, suggests **Miami Beach in Oistins** and **Bathsheba on the East Coast**.  
- This increases trip frequency and promotes **lesser-known attractions** beyond the typical tourist hotspots.  

---

## 📊 Tools and Technologies  

| Component             | Tool/Tech                  |
|-----------------------|----------------------------|
| Data Processing       | Pandas, Spark              |
| Recommendation Engine | Scikit-learn, Surprise, PyTorch |
| Storage               | Azure Cosmos DB + Delta Lake |
| Deployment            | FastAPI, Docker, Nginx     |
| Visualization         | Power BI dashboards        |
| Workflow Orchestration| GitHub Actions, DVC        |

---

## 📈 KPIs & Metrics  

- **CTR (Click-Through Rate)** on recommendations.  
- **Average rides per tourist** (should increase by ≥15%).  
- **Diversity score**: % of rides going to lesser-known POIs.  
- **Model latency**: <200ms response.  

---

## ⚠️ Risks & Mitigations  

- **Cold Start Problem**: New tourists have no history.  
  → Mitigate using popularity-based fallback + location context.  
- **Popularity Bias**: Over-promoting famous beaches.  
  → Re-rank with a diversity penalty.  
- **Data Privacy**: Sensitive ride history.  
  → Encrypt identifiers, anonymize logs.  

---

## ✅ Conclusion  

The **Tourism Recommendation Engine** transforms Bimride into a smart travel assistant for Barbados. It helps riders discover hidden gems, boosts the local economy, and creates auditable evidence of innovation for nonprofit progress tracking.  
