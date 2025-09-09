# MultiCritique: Training Language Models to Critique With Multi-agent Feedback

[![arXiv](https://img.shields.io/badge/arXiv-2410.15287-b31b1b.svg)](https://arxiv.org/abs/2410.15287)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

## 📖 Overview

**MultiCritique** is a novel data generation pipeline that enhances the critique ability of Language Models through **multi-agent feedback** in both Supervised Fine-Tuning (SFT) and Reinforcement Learning (RL) stages. 
Unlike previous approaches that rely on critiques from a single model, MultiCritique aggregates high-quality critiques from multiple agents and improves preference accuracy through multi-agent validation.
Our work addresses the key challenges in training critique-capable LLMs:
- 🧠 **Quality**: Single-model critiques often lack depth and diversity
- 🎯 **Accuracy**: Human preferences can be inconsistent and noisy
- ⚙️ **Scalability**: Human annotation is expensive and time-consuming

## ✨ Key Features

- **🤖 Multi-agent Feedback System**: Aggregates critiques from multiple LLMs to create higher quality feedback
- **🔍 Fine-grained Meta-critique**: Validates and refines critiques through detailed analysis of specific flaws
- **📊 High-quality Dataset**: MultiCritiqueDataset with diverse task scenarios (123 tasks!) and superior critique diversity
- **🚀 RL Optimization**: Novel MARV (Multi-Agent Revision Validation) mechanism for robust RL fine-tuning
- **💡 Data Efficiency**: Achieves better performance with 2.15-4.22x less training data than existing methods

## 📊 Performance Highlights

| Model | CRITICEVAL (F<sub>obj</sub>) | CRITICBENCH (Overall) |
|-------|-----------------------------|------------------------|
| **MultiCritique-7B (Ours)** | **63.28** | **75.66%** |
| GPT-3.5-turbo | 55.82 | 67.85% |
| GPT-4 | 72.41 | **78.75%** |

## 🗃️ Available Resources

We're pleased to share our trained models and datasets with the community:

### 🤗 Hugging Face Models

| Model | Description | Link |
|-------|-------------|------|
| **MultiCritique-RL-7B** | RL fine-tuned model with enhanced critique capabilities | [![Open Inference](https://img.shields.io/badge/%F0%9F%A4%97%20Model-DataHammer%2FMultiCritique--RL--7B-black?logo=huggingface)](https://huggingface.co/DataHammer/MultiCritique-RL-7B) |
| **MultiCritique-SFT-7B** | SFT fine-tuned base model with strong critique foundation | [![Open Inference](https://img.shields.io/badge/%F0%9F%A4%97%20Model-DataHammer%2FMultiCritique--SFT--7B-black?logo=huggingface)](https://huggingface.co/DataHammer/MultiCritique-SFT-7B) |

### 📚 Datasets

| Dataset | Description | Link |
|---------|-------------|------|
| **MultiCritique-SFT** | Supervised fine-tuning dataset with 32.1K high-quality critique samples | [![Open Dataset](https://img.shields.io/badge/%F0%9F%A4%97%20Dataset-DataHammer%2FMultiCritique--SFT-black?logo=huggingface)](https://huggingface.co/datasets/DataHammer/MultiCritique-SFT) |
| **MultiCritique-RL** | Reinforcement learning dataset with 19.7K preference pairs for critique quality | [![Open Dataset](https://img.shields.io/badge/%F0%9F%A4%97%20Dataset-DataHammer%2FMultiCritique--RL-black?logo=huggingface)](https://huggingface.co/datasets/DataHammer/MultiCritique-RL) |

## 📚 Citation

If you find our work useful, please cite our paper:

```bibtex
@misc{lan2024traininglanguagemodelscritique,
      title={Training Language Models to Critique With Multi-agent Feedback}, 
      author={Tian Lan and Wenwei Zhang and Chengqi Lyu and Shuaibin Li and Chen Xu and Heyan Huang and Dahua Lin and Xian-Ling Mao and Kai Chen},
      year={2024},
      eprint={2410.15287},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2410.15287}, 
}
```
