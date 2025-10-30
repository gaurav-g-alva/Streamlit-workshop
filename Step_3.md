## 3. DataFrame & Charts 
### Import these
```python
import streamlit as st
import pandas as pd
import numpy as np
```
### DataFrame
```python
df = pd.DataFrame({
    'Name': ['Alice', 'Bob', 'Charlie', 'David'],
    'Age': [25,32,37,45],
    'Occupation':['Engineer', 'Doctor','Artist','Chef']
})
#st.DataFrame(df)
st.table(df)
```
### Data Editor 
```python 
st.subheader("Data Editor")
editable_df = st.data_editor(df)
st.table(editable_df)
```
### Metrics
```python 
st.metric(label="Total Rows", value = len(df))
st.metric(label="Average Age", value = round(df['Age'].mean(),1))

```
### Chart Data
```python
chart_data = pd.DataFrame(
    np.random.randn(20,3),
    columns = ['A', 'B', 'C']
)
```
- Area Chart od chart_data
```python
st.area_chart(chart_data)
```
- Line Chart od chart_data
```python
st.line_chart(chart_data)
```
- Bar Chart od chart_data
```python
st.bar_chart(chart_data)
```

### Scatter Data

```python
scatter_data = pd.DataFrame({
    'x': np.random.randn(100),
    'y': np.random.randn(100)
})
st.scatter_chart(scatter_data)

```
### Map Data
```python
map_data = pd.DataFrame(
    np.random.randn(100, 2)/[50, 50] +[37.76, 122.4],
    columns = ['lat', 'lon']
)
st.map(map_data)
```

## 4. Status message boxes.

- <b>Success message</b>
```python
st.success("Operation Successful!")
```

- <b>Error message</b>
```python
st.error("Something went wrong.")
```
- <b>Warning message</b>
```python
st.warning("Check your input again.")
```
- <b>Info message</b>
```python
st.info("Did you know Streamlit is....")
```
<hr>

## [Home](Readme.md) || [Previous](Step_2.md) || [Next](Step_4.md) . . .