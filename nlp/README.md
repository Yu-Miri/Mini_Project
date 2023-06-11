## Installation

### Requirements
- Python==3.8

      git clone https://github.com/Yu-Miri/Mini_Project.git
      cd Mini_Project/nlp
      pip install -U sentence-transformers
    

### Preparing for DataFrame

      import pandas as pd
      from df_raw_preprocessing.py import df_preprocess

      data = pd.read_csv('Raw_data/의료사고결과.csv')
      df = pd.DataFrame(data['이유'])
      df = df.rename(columns={'이유': 'verdict'})
      df_new = df_preprocess(df)
