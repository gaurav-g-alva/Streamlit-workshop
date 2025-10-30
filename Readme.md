
### [Step 1](Step_1.md) || [Step 2](Step_2.md)
### Import these
```python

import pandas as pd
import numpy as np
import streamlit as st

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
st.table(df)
```

### Metrics
```python 
st.metric(label="Total Rows", value = len(df))
st.metric(label="Average Age", value = round(df['Age'].mean(),1))

```

## Chart Data
```python
chart_data = pd.DataFrame(
    np.random.randn(20,3),
    columns = ['A', 'B', 'C']
)

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
```
<hr>

## Form input
### Text box
```python
form_values = {
    "name": None,
    "height": None,
    "gender": None,
}


with st.form(key="user_info"):
    form_values["name"] = st.text_input("Enter your name : ")
    form_values["height"] = st.number_input("Enter your height : ")
    form_values["gender"] = st.selectbox("Gender",["Male","Female"])

    submit_button = st.form_submit_button(label="Submit")
    if submit_button:
        if not all(form_values.values()):
            st.warning("Please fill in all of the field")
```

```python
        else:
            st.balloons()
            st.write('### Info')
            for(key,value) in form_values.items():
                st.write(f"{key}:{value}")
```


### <center>---- End of the session ----
