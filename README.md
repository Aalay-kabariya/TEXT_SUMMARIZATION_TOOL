# TEXT_SUMMARIZATION_TOOL
# Abstractive Text Summarization Using BART and Streamlit  
This project focuses on **abstractive text summarization** using **BART (Bidirectional and Auto-Regressive Transformers)** from **Hugging Face’s Transformers** library. The goal is to train and deploy a model that reads long documents and generates **concise, human-like summaries**. To make it accessible, a **Streamlit web application** has been developed, enabling seamless user interaction.

## Project Details  
- **Company:** CODETECH IT SOLUTIONS  
- **Intern Name:** Aalay Kabariya 
- **Intern ID:** C0DF239 
- **Domain:** Artificial Intelligence  
- **Duration:** 4 Weeks  
- **Mentor:** Neela Santosh  

## What Was Done  
✔ **Dataset Preparation** – Loaded and split the **XSum** dataset using **Hugging Face's datasets** library.  
✔ **Model Initialization** – Used the **facebook/bart-base** pre-trained model and tokenizer.  
✔ **Data Preprocessing** – Tokenized documents and summaries with padding and truncation.  
✔ **Training Configuration** – Fine-tuned using **Hugging Face’s Trainer API** over 3 epochs.  
✔ **Model Evaluation** – Assessed performance using **ROUGE metrics**.  
✔ **Streamlit App Integration** – Developed an **interactive UI** for real-time summarization.  

## Tools and Technologies Used  
- **Python** – Core programming language  
- **BART Model (facebook/bart-base)** – Transformer-based summarization model  
- **Hugging Face datasets** – Dataset management  
- **Hugging Face transformers** – Pre-trained models & tokenizers  
- **Trainer API & TrainingArguments** – Model fine-tuning utilities  
- **ROUGE Metrics** – Summary evaluation  
- **Streamlit** – Web app framework  
- **PyTorch & CUDA** – Hardware acceleration  

## Process and Workflow  
### **Dataset Selection**  
- Used **XSum dataset**, ideal for abstractive summarization tasks.  

### **Tokenization & Preprocessing**  
- Applied **BartTokenizer** with max-length constraints:  
  - **Documents:** 256 tokens  
  - **Summaries:** 64 tokens  

### **Model Training**  
- Utilized **Trainer class** for streamlined training with:  
  - **Batch size:** 2  
  - **Epochs:** 3  
  - **Logging & evaluation strategies**  
  - **DataCollatorForSeq2Seq** for dynamic padding  

### **Model Deployment**  
- Saved fine-tuned **BART model** and deployed it via **Streamlit**.  
- Users input custom text and receive **concise AI-generated summaries**.  

### **Evaluation**  
- Computed **ROUGE scores** on test set to validate model accuracy.  

## Output  
![Image](https://github.com/user-attachments/assets/8c08f30f-a91a-42f4-a4af-65e52a3c723a)

## Installation  
```bash
git clone https://github.com/yourusername/text-summarization.git
cd text-summarization
pip install torch transformers datasets streamlit evaluate
streamlit run summarization-app.py  # Launch the app
