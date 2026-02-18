# Bayesian Inference Experiments

베이지안 추론(Bayesian Inference)을 활용해 **필요한 지점에서만 효율적으로 측정/탐색**하는 아이디어를 실험하는 저장소입니다.

## 프로젝트 개요

이 저장소에는 다양한 데이터셋과 Jupyter Notebook 실험 파일이 포함되어 있으며,
분류 문제에서의 모델 비교 및 하이퍼파라미터 탐색(예: KNN, BO 관련 실험)을 다룹니다.

## 저장소 구성

### Notebook
- `20240821_pm_Bayesian_knn_gp.ipynb` : Bayesian + KNN + GP 관련 초기 실험
- `20240912_BO_knn.ipynb` : Bayesian Optimization 기반 KNN 실험
- `20240918_multi_knn_cl.ipynb` : 다중 KNN 분류 실험
- `20250804_spiral.ipynb`, `20250804pm_spiral.ipynb` : Spiral 데이터 기반 실험

### Dataset
- `breast-cancer-wisconsin.data.csv`
- `balance-scale.data.csv`
- `haberman.data.csv`
- `sonar.all-data.csv`
- `letter-recognition.data.csv`

## 실행 방법

1. Python 가상환경 생성 및 활성화
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```
2. Jupyter 설치
   ```bash
   pip install jupyter pandas numpy scikit-learn matplotlib
   ```
3. Notebook 실행
   ```bash
   jupyter notebook
   ```

## 목적

- 불확실성을 정량화하며 학습/탐색 효율을 높이는 방법 검토
- 다양한 데이터셋에서 베이지안 기반 접근의 성능 및 특성 확인

## 참고

본 저장소는 연구/실험 목적의 Notebook 중심 프로젝트이며,
각 실험의 세부 내용은 해당 Notebook 내 마크다운/코드 셀에 기록되어 있습니다.
