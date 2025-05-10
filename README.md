# 🧠 ProSense: Defending Text Generation with Adversarial Feedback

![ProSense Diagram](assets/ProSenseCycle.png)


> A multi-stage framework to enhance LLMs' truthfulness and adversarial resilience using Graph-of-Thought reasoning and structured fine-tuning.

---

## 🚀 Overview

**ProSense** is a robust, multi-stage training framework designed to improve the truthfulness and adversarial resilience of large language models (LLMs). It leverages structured feedback in the form of Graph-of-Thought (GoT) reasoning graphs to identify and refine logical failures in model generations across curriculum-based fine-tuning cycles.

Built on a 4-bit quantized **Mistral-7B** model, ProSense incorporates adversarially generated training data and structured reasoning evaluation using **TruthfulQA**, **LLaMA**, and custom parsing logic. Training is optimized for cost-effective reproducibility on a single **A100 or H100 GPU** using **RunPod**.

---

## 🌟 Key Features

- 🔁 **Multi-Stage Fine-Tuning:** Clean, hybrid, and GoT-tagged data progressively refine model reasoning.
- ⚔️ **Adversarial Feedback Loop:** Parses and judges flawed generations to feed adversarial reasoning graphs back into training.
- 🧩 **Graph-of-Thought Parsing:** Converts flawed outputs into structured logical error paths.
- 📊 **TruthfulQA Benchmarking:** Performance evaluation using adversarial QA tasks.
- ⚙️ **GPU-Efficient Setup:** Training with 4-bit quantization on single-GPU systems.

---

## 📁 Project Structure

```plaintext
Prosense-Adversarial-Robustness/
├── Phase1_Clean_FineTuning/
│   └── phase1.ipynb
├── Phase2_Adversarial_Hybrid/
│   ├── HybridDataCreation.ipynb
│   ├── MergingWithHybridDataset.ipynb
│   └── Phase2_Final.ipynb
├── Phase3_Evaluation_Parsing/
│   ├── Phase3_1_Collect_TruthfulQA_Responses.ipynb
│   ├── Phase3_2_Judge_and_Filter_Failures.ipynb
│   ├── Phase3_3_Parse_GOT_Graph_By_LLaMA.ipynb
│   └── Phase3_Final.ipynb
└── Phase3_Level2_Refinement/
    ├── Phase4_1_Collect_Level1_Responses.ipynb
    ├── Phase4_2_Judge_Parse_Level1_By_LLaMA.ipynb
    ├── Phase4_3_Level2_Finetune.ipynb
    ├── Phase4_4_Collect_Level2_Responses.ipynb
    ├── Phase4_5_Judge_Level2_Responses.ipynb
    └── Phase4_6_Reasoning_Graph_Visualization.ipynb
