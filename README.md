# CSV to JSONL Converter for GPT Fine-Tuning

This repository provides a simple Python utility to convert datasets from **CSV format** into **JSONL format** required for **GPT fine-tuning**.  
It takes user input, system prompts, and expected outputs from a structured CSV and generates a `.jsonl` file that can be directly used in OpenAI fine-tuning workflows.

---

## 🚀 Features
- Converts CSV files with prompt/response data into JSONL format.  
- Supports both **training** and **validation** dataset preparation.  
- Lightweight and easy to run in **Google Colab** or local environments.  
- Produces an output file named `converted_data.jsonl`.  

---

## 📂 Input Format
Prepare a CSV file with **three columns**:

1. **User Input** → Input text or query from the user  
2. **Expected Output** → Target response from the model  
3. **System Prompt** → Instruction or context for the model  

👉 Example CSV: [Sample Google Sheet](https://docs.google.com/spreadsheets/d/1TcqFX9MIL1p7K6W5FRsFLww0i1bgyS00pfNqFlaeWbc/edit?usp=sharing)  

---
## 🛠️ Usage
1. Clone the repository
git clone https://github.com/your-username/csv-to-jsonl.git
cd csv-to-jsonl

2. Install dependencies
pip install pandas

3. Update file paths in the script
Open the script and replace with your dataset filename:
df = pd.read_csv("Your_File_Name.csv")
dataset = pd.read_csv("Your_File_Name.csv")

4. Run the script
python convert.py
This will generate:
converted_data.jsonl

## 📑 Example Output
Each row in the CSV is converted into JSONL format:
{"messages": [{"role": "system", "content": "System prompt"}, {"role": "user", "content": "User input"}, {"role": "assistant", "content": "Expected output"}]}

## 🎯 Fine-Tuning Workflow
Prepare training and validation datasets as CSVs.
Convert both to JSONL using this script.
Upload JSONL files to OpenAI.
Start fine-tuning your model with the prepared data.

## ⚠️ Notes
The script was originally developed in Google Colab. Some minor edits may be required if running in other environments.
Ensure your CSV file is properly formatted before conversion.

## 📜 License
MIT License
