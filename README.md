# Prosense-Defending-Text-Generation-with-Adversarial-Feedback
ProSense is a multi-stage training framework that boosts LLM truthfulness and robustness using Graph-of-Thought reasoning, adversarial feedback loops, and quantized fine-tuning on Mistral-7 B. It identifies logical failures and re-trains models through structured error correction.

🚀 Overview
ProSense is a robust adversarial defense framework for LLMs. It is built to identify and correct logical failures in model generations through structured, multi-phase training. By integrating Graph-of-Thought (GoT) reasoning graphs and adversarial feedback loops, ProSense performs progressive fine-tuning that significantly boosts truthfulness and robustness.

The pipeline is efficient, reproducible on a single A100/H100 GPU, and utilizes a 4-bit quantized Mistral-7B model with adversarial and hybrid datasets, including performance benchmarking via TruthfulQA.

🌟 Key Features
🔁 Multi-Stage Curriculum Fine-Tuning
Clean, hybrid, and GoT-tagged data progressively refine model reasoning.

⚔️ Adversarial Feedback Loop
Judging and parsing flawed outputs into adversarial reasoning graphs for targeted re-training.

🧩 Graph-of-Thought Parsing
Model failures are converted into logical trees, enabling structured learning from errors.

📊 TruthfulQA Benchmarking
Real-world adversarial evaluation to measure truthfulness improvement.

⚙️ GPU-Efficient Setup
All training runs are reproducible on a single 24 GB+ GPU using 4-bit quantized models and Unsloth.


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


