# Streamlit
---
## Import 
```Python
import streamlit as st
```

---
## Adding to our app

#### Adding a title 
```Python
st.title("Title")
```

#### Text 
```Python
st.write("""
WRITE MARKDOWN TEXT HERE
""")
```
[Markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

#### Images 
```Python
from PIL import Image

image=Image.open("filepath")

st.image(image, use_column_width=True)
```

---
## Charts 
### Linechart
```Python 
st.linechart(variable)
```

### Matplotlib graph 
```Python 
def plot(): 
	#create plot
	return st.pyplot()
```

---
## Sidebar

#### Set a header
```Python
st.sidebar.header("Header")
```

#### Dropdown list
```Python 
st.sidebar.selectbox("name", list(reversed(range(1,10))))
```

#### Selection with unique values 
```Python 
sorted_unique_team = sorted(playerstats.Tm.unique())

selected_team = st.sidebar.multiselect('Team', sorted_unique_team, sorted_unique_team)
```

### Slider
```Python
st.sidebar.slider("Name", 1, 10) #Replace 1 and 10 with the range
```

---
## Dataframe 
```Python
st.dataframe(df)
```

## Running our streamlit app 
```Terminal 
streamlit run file.py
```
---
## Forms 
```Python 
st.button('Click me')
st.checkbox('I agree')
st.radio('Pick one', ['cats', 'dogs'])
st.selectbox('Pick one', ['cats', 'dogs'])
st.multiselect('Buy', ['milk', 'apples', 'potatoes'])
st.slider('Pick a number', 0, 100)
st.select_slider('Pick a size', ['S', 'M', 'L'])
st.text_input('First name')
st.number_input('Pick a number', 0, 10)
st.text_area('Text to translate')
st.date_input('Your birthday')
st.time_input('Meeting time')
st.file_uploader('Upload a CSV')
st.download_button('Download file', data)
st.camera_input("Take a picture")
st.color_picker('Pick a color')
```
---
[Cheatsheet](https://docs.streamlit.io/library/cheatsheet)
