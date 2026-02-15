# Architectural Fragility in AI Systems  
### Failure Analysis of a Sentiment Analysis Pipeline

---

## Overview
Most machine learning projects focus only on model accuracy.  
This project explores something deeper:

**How reliable is an AI system when things go wrong?**

This study investigates how a sentiment analysis pipeline behaves under:
- Noisy input
- Corrupted data
- Distribution shifts
- Pipeline validation improvements

The goal is to understand **architectural fragility** in AI systems and how small design changes can improve robustness.

---

## Project Motivation
In real-world AI systems, failures often occur not because of poor models, but because of:
- Data quality issues
- Missing inputs
- Unexpected input formats
- Pipeline design limitations

This project demonstrates these challenges through controlled experiments.

---

## Pipeline Architecture

Raw Text
↓
Text Cleaning
↓
TF-IDF Vectorization
↓
Logistic Regression Model
↓
Prediction


---

## Experiments Conducted

### 1. Baseline Evaluation
Measured system performance under normal conditions.

### 2. Heavy Noise Injection
Simulated distribution shift by:
- Removing meaningful words
- Adding irrelevant tokens

Result: Moderate accuracy degradation.

### 3. Corrupted Input Testing
Introduced missing and invalid data to simulate real pipeline failures.

Result: Fragile pipeline failed or degraded significantly.

### 4. Robust Pipeline Implementation
Added:
- Input validation
- Fallback handling

Result: Improved reliability and stable predictions.

---

## Key Findings

- ML pipelines are sensitive to input distribution changes  
- Missing or corrupted data can cause system failures  
- Input validation significantly improves robustness  
- Architectural design impacts reliability as much as model choice  

---

## Technologies Used

- Python  
- Scikit-learn  
- Pandas  
- Matplotlib  
- Jupyter Notebook  


---

## Example Results

| Experiment | Observation |
|--------|--------|
| Baseline | Stable performance |
| Heavy Noise | Moderate accuracy drop |
| Corrupted Input | Fragile pipeline failure |
| Robust Pipeline | Stable predictions |

---

## Lessons Learned

Building a model is not enough.  
Designing **reliable ML systems** is equally important.

Key insights:
- Data quality is critical
- Validation layers prevent system crashes
- Pipeline architecture affects system stability

---

## Future Improvements

Possible extensions:
- Automatic drift detection
- Real-time monitoring
- Testing deep learning models
- Deployment simulation