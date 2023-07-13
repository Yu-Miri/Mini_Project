## Installation

### Requirements
- Python==3.8
'''
git clone https://github.com/Yu-Miri/Judgment_Recommendation_System.git
pip install -U sentence-transformers
'''

### Preparing a preprocessed dataframe
'''
import pandas as pd
from df_raw_preprocessing.py import df_preprocess

data = pd.read_csv('dataset/raw_data/의료사고결과.csv')
df = pd.DataFrame(data['이유'])
df = df.rename(columns={'이유': 'verdict'})
df_new = df_preprocess(df)
'''

### Inference

      
