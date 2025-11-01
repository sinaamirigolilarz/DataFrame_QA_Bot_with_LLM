# DataFrame Q&A Bot with LLM
**Intelligent Telegram Bot for Data Analysis with Pandas & Mistral-7B-Instruct-v0.3**

<div align="center">

[![Python](https://img.shields.io/badge/python-3.9%2B-blue)](https://www.python.org/)
[![Telegram Bot](https://img.shields.io/badge/Telegram-Bot-2CA5E0?logo=telegram)](https://core.telegram.org/bots)
[![Mistral-7B](https://img.shields.io/badge/Model-Mistral--7B--Instruct-green)](https://huggingface.co/mistralai/Mistral-7B-Instruct-v0.3)
[![GitHub stars](https://img.shields.io/github/stars/sinaamirigolilarz/DataFrame_QA_Bot_with_LLM?style=social)](https://github.com/sinaamirigolilarz/DataFrame_QA_Bot_with_LLM/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/sinaamirigolilarz/DataFrame_QA_Bot_with_LLM?style=social)](https://github.com/sinaamirigolilarz/DataFrame_QA_Bot_with_LLM/network/members)
</div>

---

## Project Overview

This project is an **intelligent Telegram bot** that lets users ask **natural-language questions in Persian** about a dataset. The bot automatically:

1. Generates **valid Pandas code**  
2. Executes the code in a **secure sandbox**  
3. Returns the result in a clean, nicely formatted response  

> **Example**  
> User: `How many people have a diploma and are married?`  
> Bot:  
> ```python
> df[(df['Educations'] == 'Diploma') & (df['Marriage'] == 'Married')].shape[0]
> ```  
> Result: `127`

---

## Key Features

| Feature | Description |
|--------|-------------|
| **Natural-Language Analysis** | Full support for Persian questions |
| **Local AI Model** | Uses `Mistral-7B-Instruct-v0.3` (no external API required) |
| **Secure Code Execution** | Restricted `eval`/`exec` with sandboxing |
| **GPU / CPU Support** | Optimized for Colab, servers, or personal machines |
| **Clean Markdown Output** | Shows question, generated code, and result professionally |
| **Works with Any Dataset** | Just replace the CSV file |

---

## Project Structure

```bash
.
├── main.ipynb                  # Main Jupyter Notebook
├── requirements.txt            # Python dependencies
├── data/
    └── df_final.csv            # Sample dataset (replaceable)
                
```
---

## Requirements

- Python 3.9 or higher  
- GPU recommended (T4 or better)  
- Telegram Bot Token from [@BotFather](https://t.me/BotFather)

---

## Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/sinaamirigolilarz/DataFrame_QA_Bot_with_LLM.git
cd DataFrame_QA_Bot_with_LLM
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Configuration
#### Dataset

Place your CSV at data/df_final.csv or update the path in the code.

#### Bot Token

Edit the following line in main.ipynb (or the generated script):

TOKEN = "YOUR_TELEGRAM_BOT_TOKEN_HERE"

---
## Result
![result 1](Screenshots/1.JPG)