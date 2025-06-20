# OCR assignment for data extraction from scanned document
A robust Python application that leverages **deep learning-based OCR** to extract structured information from scanned invoice documents. It converts raw text into clean, nested JSON format and enables intelligent, natural language querying using an integrated **Large Language Model (LLM)**.



# 🧾 AI-Powered Invoice Parser with Doctr,Flask, and Groq's LLaMA 4 model Integration

This project is a lightweight, intelligent invoice parsing tool built with **Flask, Doctr (deep learning OCR), and Groq’s LLaMA 4 model**. It allows users to upload scanned invoice images, extract structured JSON data using layout-aware OCR, and interactively query that data via a conversational interface powered by the **meta-llama/llama-4-maverick-17b-128e-instruct model**.


## 📌 Features

- 🖼️ Upload scanned or image-based invoices (supports PNG, JPG, JPEG, PDF, BMP, TIFF, and more)

- 🔍 Extract structured invoice data using Doctr, a deep learning-based OCR engine optimized for layout-aware documents

- 🗂️ Automatically generate and store clean, nested JSON output for each invoice

- 💬 Ask natural language questions about the invoice using Groq's LLaMA 4 model (meta-llama/llama-4-maverick-17b-128e-instruct)

- 🌐 Lightweight and intuitive Flask web interface with live chatbot support

---



### ✅ Prerequisites

Make sure you have the following set up before running the project:

- 🐍 Python 3.8+

- 📦 Required Python packages (see requirements.txt)

- 🔑 Groq API Key (for LLaMA model integration)

- 🌐 Active Internet connection (for API calls and model access)

- 🧠 (Optional) GPU support for faster OCR using Doctr with PyTorch backend

Note :🔒 Store your Groq API key securely in a **.env file** as GROQ_API_KEY=your_key_here

---
## 🚀 Getting Started

Follow these steps to set up and run the project locally.

---

### 📥 1. Clone the Repository

```bash
git clone https://github.com/aayushj9/OCR_assignment.git
cd OCR_assignment
```
### 🧪 2. Create and Activate Virtual Environment
```bash
# Create virtual environment
python -m venv venv

# Activate it
# On Windows
venv\Scripts\activate

# On macOS/Linux
source venv/bin/activate
```
### 📦 3. Install Dependencies
```cpp
pip install -r requirements.txt
```
### 🔐 4. Setup API Keys
```bash
GROQ_API_KEY=your_groq_api_key    # Please pass the GROQ keys in key.env file.
# if your key is passkey123  >>> pass it as  >>>GROQ_API_KEY= passkey123 
```

### ▶️ 5. Run the Flask Application
```bash
python app.py
```

Now open your browser and visit:

```cpp
http://127.0.0.1:5000
```

### ▶️ 6. Application working

```
- Choose a file and click on upload
- On left pan the extracted invoive will be shown
- On right pan the originial uploaded invovie will be shown
- On left pan bottom, Use the chatbot to ask any question
- click on clear to clear the dataset


```

### 🧾 Folder Structure
```bash
OCR_assignment/
│
├── app.py                # Main Flask app
├── invoice_utils.py      # Supporting functions
├── templates/
│   └── invoice_chat.html        # Frontend HTML form
├── static/
│   └── style.css         # Optional: CSS styling
│   └── uploads/          # Consists the invoive images
│   └── invoice_data.json # JSON outputs of parsed invoices
├── requirements.txt      # Python dependencies
├── key.env               # Grok pass keys


```


### 📝 Example Use Cases (for Chatbot)
```
"What is the total amount?”
“When is the due date?”
“Who is the vendor on this invoice?”
“What is the invoice number?”
Note : if no response available chatbot will return a sorry messge refering to right side uploaded image. 

