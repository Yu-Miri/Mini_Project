# Cafe Review Rating Predition

## 프로젝트 개요
- 기간 : 2023.01.23 ~ 2023.02.14
- 프로젝트 진행 인원 수 : 3명
- 주요 업무 및 상세 역할
      - ㅇㅇ
-----------
## Installation

#### Requirements
- Python==3.8

      git clone https://github.com/Yu-Miri/Mini_Project.git
      cd Mini_Project/text_mining
      pip install konlpy
    

#### Preparing for DataFrame

      import pandas as pd
      from df_processing import df_process
    
      reviews = pd.read_csv('reviews.csv', index_col=0, encoding='utf-8-sig')
      reviews, bow_train = df_process(reviews)
 
 
#### Modeling[[LGBM, Logistic]]
    
      from modeling import model_dataset, modeling_LGBM, modeling_Logistic
    
      X_train, X_test, y_train, y_test = model_dataset(reviews, bow_train)
      modeling_LGBM(X_train, X_test, y_train, y_test)
      modeling_Logistic(X_train, X_test, y_train, y_test)
 
 
#### Predict
Recommended procedure : Requirements -> Preparing for DataFrame -> Modeling -> Predict

      reviews['pred'] = lgbm_model.predict(X_train)
    
