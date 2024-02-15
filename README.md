# Heart Attack Analysis & Prediction
## 심장마비 분석 및 예측하기
프로젝트 기간: 2024/01/24(수) ~ 2024/02/07(수)  
<br/>
## 개요
해당 프로젝트는 심장마비에 대한 분석과 예측을 목표로 합니다. 이를 위해 "Heart Attack Analysis & Prediction Dataset"이라는 데이터셋을 활용하였습니다. 이 데이터셋은 심장마비를 분류하는 데에 사용되는 데이터를 포함하고 있습니다.  
  
이 프로젝트는 심장마비라는 의료 분야에서 중요한 문제를 해결하고자 진행되었습니다. 심장마비는 심장 기능의 장애로 인해 발생하며 생명에 직결되는 심각한 상황입니다. 이러한 이유로 프로젝트를 통해 심장마비를 사전에 예측하고 그에 대한 조치를 취함으로써 환자의 생명을 보호하고 치료 효과를 극대화하고자 하였습니다. 또한 심장마비에 대한 분석과 예측 모델을 개발함으로써 몇 가지 이익이 기대됩니다.  
  
1. 심장마비 예측 모델을 통해 의료진은 환자의 위험 정도를 사전에 파악할 수 있어 조기 진단과 치료를 진행할 수 있습니다.  
2. 환자의 건강 상태와 위험 요인을 고려하여 개인 맞춤형 치료 계획을 수립할 수 있습니다. 이를 통해 치료의 효과를 극대화하고 부작용을 최소화할 수 있습니다.  
3. 심장마비 예측 모델을 활용하여 공중보건 정책 수립이 가능해지며, 예방과 조기 대응을 위한 전략을 구축할 수 있습니다.  
  
따라서, 의료 분야에서의 중요한 문제를 해결하고 의료진과 환자 모두에게 도움이 되고자 프로젝트를 진행하게 되었습니다.
<br/>
## 사용한 데이터셋
Heart Attack Analysis & Prediction Dataset: A dataset for heart attack classification
- RASHIK RAHMAN
- https://www.kaggle.com/rashikrahmanpritom
- https://www.kaggle.com/datasets/rashikrahmanpritom/heart-attack-analysis-prediction-dataset/data
<br/>

## 프로젝트 목록
1. 소개  
    1.1 데이터 사전 설명  
    1.2 작업 목표

2. 준비  
    2.1 필요한 패키지  
    2.2 데이터 로드  
    2.3 데이터 이해하기

3. 탐색적 데이터 분석  
    3.1 단변량 분석  
    3.2 이변량 분석

4. 데이터 전처리  
    4.1 탐색적 데이터 분석을 통한 결론 도출  
    4.2 필요한 패키지  
    4.3 모델에 적합한 특성 생성

5. 모델링  
    5.1 선형 분류기  
    5.2 트리 모델
  
<br/>

## 프로젝트 수행 과정
- pandas의 read_csv 함수를 사용하여 로드한 후 데이터셋의 크기를 확인하고, 상위 5개 행을 확인하여 데이터의 구조를 파악하였습니다.
- 각 열의 고유한 값 개수를 확인하여 범주형(categorical)과 연속형(continuous) 열을 분리하였습니다.
- 'df[con_cols].describe()'를 통해 연속형 열에 대한 요약 통계량을 확인하여 데이터의 분포와 기초 통계량을 파악합니다.
- 'df.isnull().sum()'으로 결측값이 없는 것을 확인하였습니다.
- EDA의 일환으로, 단일 변수에 대해 분석하고 시각화하였습니다.
- matplotlib과 seaborn 라이브러리를 사용하여 범주형 변수에 대한 Count plot을 생성하였고, 각 변수의 카테고리별 빈도수를 시각화하여 데이터의 분포를 확인하였습니다. 이와 같은 시각화를 통해 각 변수의 분포를 확인하고 데이터의 특성을 파악하였습니다.
- 
<br/>

## 모델의 test dataset에 대한 accuracy (소숫점 다섯 째 자리에서 반올림) 
| Model | accuracy |
|:----------------------------------------|:-------|
| Support Vector Machines                 | 0.8689 |
| Hyperparameter tuning of SVC            | 0.9016 |
| Logistic Regression                     | 0.9016 |
| Decision Tree                           | 0.7869 |
| Random Forest                           | 0.7869 |
| Gradient Boosting Classifier            | 0.8689 |
<br/>

## 최종 모델
Logistic Regression
- test dataset에 대한 결과
  - accuracy: 약 0.9016
<br/>

## 결론
