

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
    
