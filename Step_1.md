# Setting Up Streamlit 

## 1. Basic Set up

- <b>Create a Directory/folder</b> <br>
open terminal
```
mkdir Streamlit-wrk
```
- <b>Open Directory/folder</b>
```
cd Streamlit-wrk
```

- <b>Create a Virtual Environment</b>

```python
python -m venv venv
source venv/bin/activate   # For Linux/Mac
venv\Scripts\activate      # For Windows
```
<code style="color : red">If there's any Error in Activating Virtual Environment in Windows then use below code (Temporary fix) and run the venv\Scripts\activate </code>
```
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope Process
```
- <b>Install the Required Libs</b>

```python 
pip install streamlit
pip install pandas
pip install numpy
```
<hr>

## [Home](Readme.md) || [Next](Step_2.md) . . . 
