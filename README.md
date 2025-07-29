# DFChat

DFChat is an interactive LLM-based solution for Exploratory Data Analysis (EDA) that allows analyze your data using natural language.

## Features

* Natural language interaction with Pandas DataFrames
* Automatic graph generation based on questions asked
* On-demand descriptive statistical analysis
* Support for multiple LLM models (such as Deepseek, LLaMA, etc.) using [Groq](https://groq.com/)
* Easy integration with notebooks

## Installation

1. Clone this repository

```bash
git clone https://github.com/fernandozagatti/DFChat.git
cd DFChat
```

2. Install the dependencies

```bash
pip install -r requirements.txt
```

3. (Optional) Configure your Groq API Key for the language model

```bash
export GROQ_API_KEY="your-key-here"
```

## How to use

First, you need to create a [Groq API Key](https://console.groq.com/keys).

After that, import your data into a Pandas DataFrame and call DFChat, as shown in the following example:

```python
import sys
sys.path.append('src')
import pandas as pd
from dfchat import DFChat

df = pd.read_csv("your_data.csv")
chat_llm = DFChat(df)
response = chat_llm.chat("Tell me about the data")
```