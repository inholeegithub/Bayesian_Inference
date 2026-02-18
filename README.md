# Bayesian Inference Experiments

This repository explores ideas for using **Bayesian Inference** to perform measurement and exploration **efficiently, only where needed**.

## Project Overview

The repository includes multiple datasets and Jupyter Notebook experiments, covering
model comparisons and hyperparameter search in classification tasks (e.g., KNN and Bayesian Optimization experiments).

## Repository Structure

### Notebooks
- `20240821_pm_Bayesian_knn_gp.ipynb`: Early experiments related to Bayesian + KNN + GP
- `20240912_BO_knn.ipynb`: KNN experiments based on Bayesian Optimization
- `20240918_multi_knn_cl.ipynb`: Multi-KNN classification experiments
- `20250804_spiral.ipynb`, `20250804pm_spiral.ipynb`: Experiments using spiral data

### Datasets
- `breast-cancer-wisconsin.data.csv`
- `balance-scale.data.csv`
- `haberman.data.csv`
- `sonar.all-data.csv`
- `letter-recognition.data.csv`

## How to Run

1. Create and activate a Python virtual environment
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```
2. Install Jupyter and required libraries
   ```bash
   pip install jupyter pandas numpy scikit-learn matplotlib
   ```
3. Launch Jupyter Notebook
   ```bash
   jupyter notebook
   ```

## Goals

- Explore methods to improve learning/search efficiency while quantifying uncertainty
- Evaluate performance and characteristics of Bayesian-based approaches across various datasets

## Notes

This repository is a notebook-centered project for research and experimentation.
Detailed descriptions of each experiment are documented in the markdown/code cells of each notebook.

## KNN 기반 스캔 방식 Mermaid Diagram

```mermaid
flowchart TD
    A[스캔 시작 요청] --> B[데이터 수집 및 전처리]
    B --> C[스캔 포인트 후보 생성]
    C --> D[KNN 모델에 후보 입력]
    D --> E{최근접 이웃 거리/밀도 기준 충족?}
    E -- 예 --> F[고신뢰 영역으로 판단]
    E -- 아니오 --> G[불확실 영역으로 판단]
    F --> H[스캔 간격 확대]
    G --> I[스캔 간격 축소]
    H --> J[다음 스캔 지점 선택]
    I --> J
    J --> K[측정값 업데이트 및 DB 저장]
    K --> L{종료 조건 충족?}
    L -- 아니오 --> C
    L -- 예 --> M[스캔 종료 및 결과 리포트]
```
