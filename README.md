# 💳 Credit Scoring Model Optimization Project
> 불균형 금융 데이터를 활용한 연체 예측 및 신용 점수 산출 시스템 구축

## 1. Project Overview
본 프로젝트는 고객의 금융 거래 이력을 바탕으로 연체 여부를 예측하고, 이를 정량적인 신용 점수로 변환하는 모델링 과정을 담고 있습니다. 특히, 실무 금융 환경에서 발생하는 데이터 불균형 문제를 해결하고 리스크 관리 효율을 극대화하는 데 초점을 맞추었습니다.

## 2. Key Challenges & Solutions
- **Data Imbalance:** 연체자 비중이 매우 적은(6.6%) 문제를 해결하기 위해 SMOTE와 모델 가중치(`scale_pos_weight`) 조절을 병행했습니다.
- **Model Evolution:** - Baseline: Logistic Regression (Recall 0.70, Precision 0.16)
  - Advanced: Random Forest (AUC-ROC 0.829, Recall 0.31)
  - Final: **XGBoost** (Recall 0.76, Precision 0.23, AUC-ROC 0.86)
    - scale_pos_weight & Threshold Tuning으로 리스크 관리 최적화 -> (Recall 0.67, Precision 0.3)
- **Business Logic:** 단순 분류를 넘어 확률값을 300~1000점 체계의 Credit Score로 변환하는 알고리즘을 구현했습니다.

## 3. Tech Stack
- Python (Pandas, Scikit-learn, XGBoost)
- Visualization (Matplotlib, Seaborn)
- Deployment (Joblib)

## 4. Conclusion
"정확도(Accuracy)의 함정에 빠지지 않고, 금융 도메인에서 중요한 Recall을 0.76까지 끌어올려 실질적인 리스크 관리 지표를 제시했습니다."