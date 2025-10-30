## 5. User Input Widgets
### st.button() - Creates a clickable button.
```python
if st.button("Click Me"):
    st.write("Button clicked!")
```
### st.text_input() - Takes text input from the user.
```python
name = st.text_input("Enter your name:")
st.write("Hello", name)
```
### st.number_input() - Takes numeric input (int/float).
```python
age = st.number_input("Enter your age:", min_value=1, max_value=100)
st.write("You are", age, "years old.")
```
### st.text_area() - Multi-line text input.
```python
feedback = st.text_area("Write your feedback:")
```
### st.date_input() - Takes a date input.
```python
date = st.date_input("Select your Date ")
st.write("Date:", date)
```
### st.time_input() - Takes time input.
```python
time = st.time_input("Select time")
```
### st.slider() - Creates a slider for numeric range.
```python
level = st.slider("Select difficulty level", 0, 10, 5)
st.write("Level:", level)
```
### st.selectbox() - Dropdown menu (single selection).
```python
option = st.selectbox("Choose your language", ["Python", "C++", "Java"])
st.write("You selected:", option)
```
### st.multiselect() - Dropdown menu (multiple selections).
```python
skills = st.multiselect("Select your skills", ["Python", "JS", "C++"])
st.write("You chose:", skills)
```
### st.checkbox() - Checkbox for boolean input.
```python
agree = st.checkbox("I agree to terms and conditions")
if agree:
    st.success("Thank you!")
```
### st.radio() - Select one option from a list (radio buttons).
```python
gender = st.radio("Select gender:", ["Male", "Female", "Other"])
st.write("Gender:", gender)
```
### st.file_uploader() - Allows uploading of files.
```python
file = st.file_uploader("Upload a CSV file", type=["csv"])
if file:
    import pandas as pd
    df = pd.read_csv(file)
    st.dataframe(df)
```
<hr>

## [Home](Readme.md) || [Previous](Step_3.md) || [Next](Step_5.md) . . .