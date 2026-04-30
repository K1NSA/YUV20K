# [YUV20K: A Complexity-Driven Benchmark and Trajectory-Aware Alignment Model for Video Camouflaged Object Detection]

[![Paper](https://img.shields.io/badge/arXiv-Paper-B31B1B?style=flat-square&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2604.09985)
[![Dataset: YUV20K](https://img.shields.io/badge/Dataset-Google_Drive-4285F4?style=flat-square&logo=googledrive&logoColor=white)](https://drive.google.com/file/d/1Iu5SI3CAQz5Zz293_aRpuo40O5NaTtkB/view?usp=sharing)
[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey?style=flat-square)](https://creativecommons.org/licenses/by-nc/4.0/)


**YUV20K Dataset.**

> **Brief Introduction:** We introduce a novel framework for Video Camouflaged Object Detection (VCOD). To tackle motion-induced feature instability, we propose the **Motion Feature Stabilization (MFS)** and to tackle temporal feature misalignment, we propose **Trajectory-Aware Alignment (TAA)** modules. Furthermore, we contribute **YUV20K**, a new large-scale , complexity-driven dataset to advance VCOD research.

---

## 📅 Project Roadmap & Updates

| Date | Event | Status |
| :--- | :--- | :---: |
| 2026-04 | Paper submission | ✅ |
| 2026 | Release YUV20K dataset | ✅ |
| 2026 | Release source code |  |



---
## 📑 Table of Contents
- [Highlights](#-highlights)
- [The YUV20K Dataset](#-the-yuv20k-dataset)
- [Dataset Show](#-dataset-show)
- [Architecture & Implementation](#-architecture--implementation)
- [Quantitative Comparison](#-quantitative-comparison)

---

## 🌟 Highlights

1. **New Dataset (YUV20K):** A comprehensive video dataset specifically curated for complex challenging VCOD scenarios.
2. **Trajectory-Aware Alignment (TAA):** Accurately predict object motion trajectories to align temporal features.
3. **Motion Feature Stabilization (MFS):** Utilizes Semantic Basis Primitives (SBPs) to stabilize features against motion-induced distortions.

---

## 📀 The YUV20K Dataset
<img width="644" height="260" alt="image" src="https://github.com/user-attachments/assets/b3065833-87a4-4b47-a2d2-eefe4fa7f3be" />

We release **YUV20K**, providing high-quality annotations for complex camouflaged videos.

* **Agreement:** License & Terms of Use (许可与使用条款)

The YUV20K dataset is available under the CC BY-NC 4.0 License (知识共享署名-非商业性使用 4.0 国际许可协议).

Disclaimer (免责声明):
The raw videos included in this dataset are collected from public internet sources (e.g., documentaries). The copyright of these videos belongs to their original creators/owners. This dataset is compiled strictly for academic research purposes only (仅供学术研究使用) under the principle of Fair Use (合理使用). Any commercial usage of this dataset is strictly prohibited. If you are a copyright owner and wish to have your content removed, please contact us, and we will delete it immediately.
（本数据集包含的原始视频均收集自公开网络来源。这些视频的版权归其原始创作者/所有者所有。本数据集的构建严格遵循“合理使用”原则，仅供学术研究使用。严禁将本数据集用于任何商业用途。如果您是版权所有者并希望移除您的内容，请与我们联系，我们将立即删除。）
* **Download Link:** (https://drive.google.com/file/d/1Iu5SI3CAQz5Zz293_aRpuo40O5NaTtkB/view?usp=sharing)

---
## 🎬 Dataset Show
### 🖼️ Static Images
<div align="center">
  <img width="761" height="453" alt="dataset_image" src="https://github.com/user-attachments/assets/3c0c9fb5-2904-4c09-9ec2-2e11391cbba1" />
</div>

---

### 🎞️ Dynamic GIFs
<table>
  <tr>
    <td align="center">
      <img width="512" height="288" alt="horn_shark angel_shark" src="https://github.com/user-attachments/assets/33af8311-2ddd-44ca-a3b2-4534c7498d74" />
    </td>
    <td align="center">
      <img width="512" height="288" alt="octopus_3" src="https://github.com/user-attachments/assets/9cad437c-de6a-4960-b37f-1046dd1833db" />
    </td>
  </tr>
  <tr>
    <td align="center">
      <img width="512" height="288" alt="eastern_screech_owl_1" src="https://github.com/user-attachments/assets/40822bb6-d16a-4584-9e1b-f7375b0edb6f" />
    </td>
    <td align="center">
      <img width="512" height="288" alt="savanna nightjar_2" src="https://github.com/user-attachments/assets/906b659d-6622-464c-9a3b-d28046f5d5a8" />
    </td>
  </tr>
  <tr>
    <td align="center">
      <img width="512" height="288" alt="leaf_insects_2" src="https://github.com/user-attachments/assets/dffe0b83-170e-4dda-88a3-3ed977543b03" />
    </td>
    <td align="center">
      <img width="512" height="288" alt="spider_tailed_horned_viper_1" src="https://github.com/user-attachments/assets/341f4d6a-38c2-42c5-b4ec-3a3efc1d38cc" />
    </td>
  </tr>
</table>

--

## 🧠 Architecture & Implementation
<img width="766" height="347" alt="structure" src="https://github.com/user-attachments/assets/1e0c495e-d0c4-4e35-8755-513c0245b278" />



### 🔑 Key Hyperparameter Settings (Tips for Reproduction)
To achieve optimal performance on different datasets, we strongly recommend the following parameter configurations in your `config.yaml`:

* **SBP Dimension:** The dimension of Semantic Basis Primitives (SBP) is optimally set to **`384`**.
* **Theta ($\theta$) Value Adjustment:** The parameter $\theta$ in our alignment module is sensitive to dataset characteristics. We recommend:
  * For **MoCA** dataset: `theta = 0.458`
  * For **YUV** dataset: `theta = 0.158`
*(Note: In future work, $\theta$ can be extended as a learnable parameter rather than a fixed scalar.)*



### 📈 Quantitative Comparison
Our method achieves state-of-the-art performance on the **YUV20K** and **MoCA-Mask** benchmarks.
<img width="770" height="207" alt="image" src="https://github.com/user-attachments/assets/29af2eac-3959-414c-9879-fe0d8ee0cdd1" />




