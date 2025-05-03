# Dashboard Polusi Udara Beijing ✨
## Run a Streamlit App on Google Colab Notebook
- Buka google Collabs https://colab.research.google.com/
## Install Streamlit library
```
!pip install -q streamlit
```
## Create/Run a streamlit app example code
Jalankan kode yang saya buat
```
%%writefile dashboard.py

import streamlit as st

def create_bycity_df(df):
    bycity_df = df.groupby(["year","station"]).mean(numeric_only =True).reset_index()
    return bycity_df

# dan selanjutnya copykan semua
```

## Install localtunnel to serve the Streamlit app
```
!npm install localtunnel
```

## Run the Streamlit app in the background
```
!streamlit run dashboard.py &>/content/logs.txt &
```

## Expose the Streamlit app on port 8501
```
!npx localtunnel --port 8501 & curl https://loca.lt/mytunnelpassword
```
Then just click in the url showed and input your password and it will generate to streamlit app.
