## 2. Text & Headings

### Create a python file " main.py"
- <b>Import Streamlit</b>
```
import streamlit as st
```

- <b>Main title of the app.</b>
```
st.title("Streamlit Workshop")
```

- <b>Section heading.</b>
```
st.header("Hello world")
```
- <b>Sub-section heading.</b>
```
st.subheader("This is SubSection")
```

- <b>Displays plain text (no formatting).</b>
```
st.text("This is a simple text line.")
```

- <b>Displays formatted text (Markdown supported).</b>
```
st.markdown("**Bold text**, _italic text_, and `code`")
```

- <b> write - Universal function  automatically detects data type and displays it appropriately.</b>
```
st.write("Hello World!")
st.write(123)
st.write({"A": 10, "B": 20})
```

- <b>Small caption text.</b>
```
st.caption("Built using Streamlit")
```


- <b>Displays code with syntax highlighting.</b>
```
st.code("for i in range(5): st.write(i)", language="python")
```
<hr>

## [Home](Readme.md) || [Previous](Step_1.md) || [Next](Step_3.md) . . .