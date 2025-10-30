## 6. Form input
### Dictionary
```python
form_values = {
    "name": None,
    "height": None,
    "gender": None,
}
```
### Creating a form
```python
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
<hr>

## [Home](Readme.md) || [Previous](Step_4.md)

### <center>---- End of the session ----