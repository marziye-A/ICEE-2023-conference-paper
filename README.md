---
```markdown
#  Speech Emotion Recognition Using Transfer Learning and Self-Supervised Speech Representation Learning 

[!Paper](https://ieeexplore.ieee.org/document/10334799)

This repository contains the official implementation of the research paper:  
"Speech Emotion Recognition Using Transfer Learning and Self-Supervised Speech Representation Learning" (Published in the 31st International Conference on Electrical Engineering - ICEE, 2023).

## 📖 Abstract

Self-supervised speech representation learning (S3RL) models like wav2vec2.0, HuBERT, and WavLM offer powerful general-purpose speech representations. However, their massive parameter counts make fine-tuning challenging for low-resource tasks such as Speech Emotion Recognition (SER). 

To address this, we propose a lightweight architecture that leverages the pre-trained HuBERT convolutional feature encoder but replaces the computationally expensive Transformer layers with a streamlined Conformer block structure. Our results demonstrate that this compact model achieves performance comparable to much larger S3RL models while being significantly more efficient for low-resource emotional speech tasks.

## 🏗️ Architecture

The proposed model architecture follows a hybrid approach:

1.  Feature Extraction: We utilize the pre-trained convolutional feature encoder from the HuBERT model to capture local acoustic features.
2.  Sequence Modeling: Instead of the standard HuBERT Transformer layers, we implement a series of Conformer blocks. The Conformer combines Convolutional neural networks and Transformers to capture both local and global dependencies more efficiently.
3.  Task Head: A lightweight classification head designed for emotion category prediction.

<img width="183" height="527" alt="image" src="https://github.com/user-attachments/assets/6f019d3c-b38c-4b1d-8165-f878ce49ca67" />



## 🚀 Key Features

- Weight Efficiency: Drastically reduced parameter count compared to full HuBERT/WavLM fine-tuning.
- Hybrid Modeling: Leverages the CNN strengths of HuBERT and the dual-domain strengths of Conformer.
- Low-Resource Ready:* Optimized for datasets where training large-scale models is computationally prohibitive.

## 🛠️ Installation

# Clone the repo
git clone https://github.com/marziye-A/ICEE-2023-conference-paper.git
cd ICEE-2023-conference-paper

# Install dependencies
pip install -r requirements.txt
