# MedBot
A conversational AI model for answering general queries related to medical and healthcare field
Here’s a clean **README.md** draft for your notebook project:

---

# 🩺 Medical Question Answering with Transformers

This repository contains a Kaggle-based notebook for building and fine-tuning a **Medical Question Answering** model using the **MedQuAD dataset**. The project leverages **Hugging Face Transformers**, **PEFT (Parameter-Efficient Fine-Tuning)**, and **TRL** to create an efficient and accurate question-answering system for the medical domain.

---

## 📂 Dataset

We use the **[MedQuAD Dataset](https://www.kaggle.com/datasets/)**, which contains medical question-answer pairs across multiple focus areas.

* **File:** `medquad.csv`
* **Columns include:**

  * `focus_area` → Medical domain (e.g., cardiology, dermatology)
  * `question` → User question
  * `answer` → Ground-truth medical response

---

## ⚙️ Workflow

1. **Data Loading & Cleaning**

   * Read `medquad.csv` into a Pandas DataFrame.
   * Handle missing values and split into train/validation sets.

2. **Environment Setup**

   * Install dependencies:

     ```bash
     pip install --upgrade kagglehub[pandas-datasets,hf-datasets]
     pip install -U transformers peft accelerate datasets bitsandbytes trl
     ```

3. **Model & Training**

   * Load pre-trained transformer models (`AutoModelForCausalLM`, `AutoTokenizer`).
   * Apply **LoRA fine-tuning** with PEFT for efficient training.
   * Train using **SFTTrainer** from Hugging Face TRL.

4. **Evaluation**

   * Evaluate on validation set.
   * Check focus-area distributions and response quality.

---

## 🛠️ Dependencies

* Python 3.10+
* [Transformers](https://huggingface.co/docs/transformers/)
* [PEFT](https://huggingface.co/docs/peft/)
* [Datasets](https://huggingface.co/docs/datasets/)
* [TRL](https://huggingface.co/docs/trl/)
* [KaggleHub](https://github.com/Kaggle/kagglehub)

---

## 🚀 Usage

Run the notebook step by step in **Kaggle** or **Jupyter**:

```bash
jupyter notebook medical-question-answer.ipynb
```

For training on GPU:

```python
trainer.train()
```

---

## 📊 Results

* Model fine-tuned on medical QA dataset.
* Supports specialized domains like **cardiology, oncology, neurology, etc.**
* LoRA reduces training costs while preserving performance.

---

## 📌 Notes

* This project is for **educational and research purposes only**.
* Not a replacement for professional medical advice.

---

## 👨‍💻 Author

Developed by **Arnab Chatterjee**

---



