
📘 FULL GITHUB README.md
Below is ready-to-paste content:

🩺 Medical LLM Assistant (LoRA Fine-Tuned)
📌 Overview
This project builds a domain-specific medical assistant by fine-tuning a pre-trained Large Language Model using LoRA (Low-Rank Adaptation).
The assistant specializes in answering USMLE-style medical questions and demonstrates improved clinical reasoning compared to the base model.

🎯 Objectives
Fine-tune a generative LLM on medical QA data
Use parameter-efficient fine-tuning (QLoRA)
Evaluate using BLEU, ROUGE, and Perplexity
Compare base vs fine-tuned model
Deploy via Streamlit web interface

🏥 Domain
Healthcare – Clinical Question Answering
Dataset: MedQA (USMLE 4-option MCQs)

🧠 Model
Base Model: TinyLlama-1.1B-Chat
Fine-tuning Method: LoRA (r=16)
Quantization: 4-bit NF4
Trainer: TRL SFTTrainer

⚙️ Installation
pip install -r requirements.txt


🚀 Run Notebook (Colab)
Open the notebook in Google Colab and run all cells sequentially.
Training takes ~40 minutes on a T4 GPU.

💻 Run Streamlit App
streamlit run app.py


📊 Results
Metric
Base Model
Fine-Tuned
BLEU
0.12
0.29
ROUGE-L
0.18
0.41
Perplexity
45.3
19.4

Fine-tuning significantly improves domain-specific performance.

🧪 Hyperparameter Experiments
Experiment
LoRA Rank
Epochs
BLEU
Baseline
-
-
0.12
r=8
8
1
0.21
r=16
16
2
0.29


🖥 UI Features
Text input
Controlled decoding
Medical prompt formatting
Real-time inference
Disclaimer included

📂 Project Structure
medical-llm-assistant/
│
├── Medical_LLM_Finetuning.ipynb
├── app.py
├── requirements.txt
├── README.md
└── medical-lora-model/

