# Streamlit Components

Components are third-party Python modules that extend what's possible with Streamlit [[1](https://docs.streamlit.io/library/components)].

## What Streamlit components are available?

There are several dozens of Streamlit components featured on Streamlit's website [[2](https://streamlit.io/components)].

Fanilo (a Streamlit Creator) curated an amazing list of Streamlit components on a wiki post [[3](https://discuss.streamlit.io/t/streamlit-components-community-tracker/4634)] that lists about 85 Streamlit components as of April 2022.

## How to use?

Streamlit components are just a pip-install away.

In this tutorial, let's get you started in using the `streamlit_pandas_profiling` component [[4](https://share.streamlit.io/okld/streamlit-gallery/main?p=pandas-profiling)].

#### Install the component 

```bash
pip install streamlit_pandas_profiling
```

## Demo app

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/st.template/)

## Code
Here's how to use st.write:
```python
import streamlit as st
import pandas as pd
import pandas_profiling
from streamlit_pandas_profiling import st_profile_report

st.header('`streamlit_pandas_profiling`')

df = pd.read_csv('https://raw.githubusercontent.com/dataprofessor/data/master/penguins_cleaned.csv')

pr = df.profile_report()
st_profile_report(pr)
```

## Line-by-line explanation
The very first thing to do when creating a Streamlit app is to start by importing the `streamlit` library as `st` as well as other libraries used in the app like so:
```python
import streamlit as st
import pandas as pd
import pandas_profiling
from streamlit_pandas_profiling import st_profile_report
```

This is followed by creating a header text for the app:
```python
st.header('`streamlit_pandas_profiling`')
```


## Further reading
1. [Streamlit Components - API Documentation](https://docs.streamlit.io/library/components)
2. [Featured Streamlit Components](https://streamlit.io/components)
3. [Streamlit Components - Community Tracker](https://discuss.streamlit.io/t/streamlit-components-community-tracker/4634)
4. [`streamlit_pandas_profiling`](https://share.streamlit.io/okld/streamlit-gallery/main?p=pandas-profiling)
