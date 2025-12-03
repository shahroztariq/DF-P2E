# We are working on version 2.0 of our DF-P2E tool and will share it soon.

# 🧠 DF-P2E: From Prediction to Explanation  
**From Prediction to Explanation: Multimodal, Explainable, and Interactive Deepfake Detection Framework for Non-Expert Users**  
📍 *ACM Multimedia 2025 (ACM MM '25), Dublin, Ireland*

## 🔍 Overview
**DF-P2E** (Deepfake: Prediction to Explanation) is a novel multimodal framework designed to make deepfake detection interpretable, accessible, and interactive, especially for non-expert users in forensic, journalistic, and legal contexts.

Unlike traditional black-box classifiers, DF-P2E integrates **visual**, **semantic**, and **narrative** layers of explanation to bridge the gap between prediction and human understanding.

## 🧩 Key Components

DF-P2E consists of three modular components:

1. **Deepfake Classifier**  
   - Uses Grad-CAM to generate saliency maps highlighting manipulated regions.  
   - Backbone: CLIP-large (best AUC on DF40 benchmark).

2. **Visual Captioning Module**  
   - Converts saliency maps into natural language descriptions.  
   - Powered by BLIP-large for optimal balance between quality and efficiency.

3. **Narrative Refinement Module**  
   - Uses a fine-tuned LLaMA-3.2-11B-Vision model.  
   - Produces context-aware, user-sensitive explanations tailored to forensic and public-facing applications.

## 🧪 Experimental Highlights

- **Dataset**: DF40 (40 manipulation techniques, diverse sources).
- **Detection Performance**:  
  - CLIP-large achieves **AUC = 0.913**, outperforming XceptionNet and CLIP-base.
- **Captioning Quality**:  
  - BLIP2-Flan-T5-xxl achieves the highest CIDEr score (1.461), but BLIP-large is selected for deployment due to speed and fluency.
- **Human Evaluation**:  
  - Average scores:  
    - Usefulness: 4.5  
    - Understandability: 4.0  
    - Explainability: 4.0  
  - Participants praised the layered explanation pipeline and natural language narratives.

## 🎯 Use Case

> An investigator receives an image as evidence and wants to know if it's real or fake.  
> DF-P2E analyses the image, classifies it, explains why (via heatmap, caption, and narrative), and allows the user to interact with the system to clarify doubts.

## 📺 Demo & Walkthrough
- 🎥 [Video Walkthrough](https://zenodo.org/records/15198666) 
- 🔗 [Live Demo]() Coming Soon

## 📄 Citation
If you use DF-P2E in your research, please cite:
```bibtex
@inproceedings{tariq2025dfp2e,
  author    = {Shahroz Tariq and Simon S. Woo and Priyanka Singh and Irena Irmalasari and Saakshi Gupta and Dev Gupta},
  title     = {From Prediction to Explanation: Multimodal, Explainable, and Interactive Deepfake Detection Framework for Non-Expert Users},
  booktitle = {Proceedings of the 33rd ACM International Conference on Multimedia (ACM MM '25)},
  year      = {2025},
  doi       = {10.1145/3746027.3755786}
}
