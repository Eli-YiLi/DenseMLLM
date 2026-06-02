# DenseMLLM: Standard Multimodal LLMs for Dense Prediction

<div align="center">

[![Paper](https://img.shields.io/badge/Paper-ICML2026-B31B1B.svg)](https://openreview.net/forum?id=F99QbhItQE)
[![arXiv](https://img.shields.io/badge/arXiv-Youtu--VL:Tech_Report-007EC2.svg)](https://arxiv.org/abs/2601.19798)
[![HuggingFace](https://img.shields.io/badge/%F0%9F%A4%97%20HuggingFace-Model_Download-FF9147.svg)](https://huggingface.co/tencent/Youtu-VL-4B-Instruct)
[![GitHub](https://img.shields.io/badge/GitHub-Code_Repos-181717.svg)](https://github.com/TencentCloudADP/youtu-vl)

</div>

---

## 📄 Abstract

Multimodal Large Language Models (MLLMs) have shown exceptional high-level vision-language understanding. However, extending them to fine-grained **dense prediction** tasks (e.g., segmentation, depth estimation) typically requires complex, task-specific decoders, fragmenting the model architecture.

**DenseMLLM** challenges this paradigm. We demonstrate that a standard MLLM architecture, with appropriate supervision, can inherently function as a dense predictor. Our method introduces a novel **multi-label vision token supervision strategy** that extends the Next-Token Prediction (NTP) paradigm from text to vision tokens. This allows the model to handle the multi-semantic nature of visual tokens and perform high-quality dense predictions directly, without any architectural specializations.

### Core Contributions
1.  **Standard MLLM for Dense Tasks**: We eliminate the need for external decoders (like SAM or Mask2Former) by extracting dense predictions directly from the vision tokens of a standard MLLM.
2.  **Vision NTP-M**: We propose a multi-label autoregressive loss that allows a single vision token to correspond to multiple semantic labels, enabling robust optimization for diverse dense tasks.
3.  **Unified Architecture**: DenseMLLM is a general-purpose foundation model that excels in both traditional VQA tasks and pixel-level dense perception without compromising architectural simplicity.

---

## 📢 Statement

This repository and the associated research are presented under the name **DenseMLLM** for the purpose of submission to **ICML 2026**.

**1. Relationship between DenseMLLM and Youtu-VL:**
The work disclosed here constitutes the **Dense Prediction** component of the **Youtu-VL** model series. The naming convention "DenseMLLM" is adopted strictly to highlight the core scientific contribution of this specific submission—demonstrating that standard MLLMs can intrinsically serve as dense predictors without architectural modifications.

**2. Anonymity & Attribution:**
To comply with the double-blind review policy of the conference, the main text and repository refer to the model as DenseMLLM to avoid revealing the identity of the authors. However, for the sake of transparency and completeness regarding the model's architecture and training pipeline, we direct readers to the comprehensive technical report.

**3. Full Disclosure:**
For detailed information regarding the model's pre-training data, extended multi-task capabilities, and full architectural specifications beyond dense prediction, please refer to the **Youtu-VL technical report** linked below. The model weights released on Hugging Face correspond to the Youtu-VL project.

---

## 📚 Citation

If you find our work useful, please cite both the conference paper (for the dense prediction methodology) and the technical report (for the full model details).

### DenseMLLM (ICML 2026)
For research specifically focusing on dense prediction, vision token supervision, and the standard architecture paradigm.

```bibtex
@misc{li2026densemllmstandardmultimodalllms,
      title={DenseMLLM: Standard Multimodal LLMs for Dense Prediction}, 
      author={Yi Li and Hongze Shen and Lexiang Tang and Xin Li and Xinpeng Ding and Yinsong Liu and Deqiang Jiang and Xing Sun and Xiaomeng Li},
      year={2026},
      eprint={2602.14134},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2602.14134}, 
}
```

### Youtu-VL (Technical Report)
For research requiring details on the full model pre-training, data recipes, or the broader Youtu-VL framework.
```
@article{wei2026youtu,
  title={Youtu-VL: Unleashing Visual Potential via Unified Vision-Language Supervision},
  author={Wei, Zhixiang and Li, Yi and Kan, Zhehan and Jiang, Xinghua and Long, Zuwei and Liu, Shifeng and Shen, Hongze and Liu, Wei and Tan, Xiaoyu and Lin, Haojia and others},
  journal={arXiv preprint arXiv:2601.19798},
  year={2026}
}
```
