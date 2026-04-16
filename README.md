# [YUV20K: A Complexity-Driven Benchmark and Trajectory-Aware Alignment Model for Video Camouflaged Object Detection]

[![Paper](https://img.shields.io/badge/arXiv-Paper-B31B1B?style=flat-square&logo=arxiv&logoColor=white)]()
[![Dataset: YUV20K](https://img.shields.io/badge/Dataset-YUV20K-06A7FF?style=flat-square&logo=baidu&logoColor=white)]()
[![License](https://img.shields.io/badge/License-MIT-green.style=flat-square)]()

**YUV20K Dataset.**

> **Brief Introduction:** We introduce a novel framework for Video Camouflaged Object Detection (VCOD). To tackle motion-induced feature instability, we propose the **Motion Feature Stabilization (MFS)** and to tackle temporal feature misalignment, we propose **Trajectory-Aware Alignment (TAA)** modules. Furthermore, we contribute **YUV20K**, a new large-scale , complexity-driven dataset to advance VCOD research.

---

## 📑 Table of Contents
- [Highlights](#-highlights)
- [The YUV20K Dataset](#-the-yuv20k-dataset)
- [Architecture & Implementation](#-architecture--implementation)
- [Getting Started](#-getting-started)
- [Citation & Contact](#-citation--contact)

---

## 🌟 Highlights

1. **New Dataset (YUV20K):** A comprehensive video dataset specifically curated for complex challenging VCOD scenarios.
2. **Trajectory-Aware Alignment (TAA):** Accurately predict object motion trajectories to align temporal features.
3. **Motion Feature Stabilization (MFS):** Utilizes Semantic Basis Primitives (SBPs) to stabilize features against motion-induced distortions.

---

## 📀 The YUV20K Dataset
<img width="644" height="260" alt="image" src="https://github.com/user-attachments/assets/b3065833-87a4-4b47-a2d2-eefe4fa7f3be" />

We release **YUV20K**, providing high-quality annotations for complex camouflaged videos.

* **Access:** The dataset is hosted on Baidu Netdisk and Google Drive. 
* **Agreement:** To protect the data, please fill out the [Data Access Agreement](./assets/Agreement.pdf) (CC BY-NC 4.0) and email us for the unzip password.
* **Download Link:** [Baidu Netdisk (Pwd: xxxx)]()

---
## 🎬 Dataset Show
<img width="766" height="347" alt="image" src="https://github.com/user-attachments/assets/1e0c495e-d0c4-4e35-8755-513c0245b278" />


<img width="512" height="288" alt="horn_shark angel_shark" src="https://github.com/user-attachments/assets/33af8311-2ddd-44ca-a3b2-4534c7498d74" />

<img width="512" height="288" alt="octopus_3" src="https://github.com/user-attachments/assets/9cad437c-de6a-4960-b37f-1046dd1833db" />


<img width="512" height="288" alt="eastern_screech_owl_1" src="https://github.com/user-attachments/assets/40822bb6-d16a-4584-9e1b-f7375b0edb6f" />

<img width="512" height="288" alt="savanna nightjar_2" src="https://github.com/user-attachments/assets/906b659d-6622-464c-9a3b-d28046f5d5a8" />

<img width="512" height="288" alt="leaf_insects_2" src="https://github.com/user-attachments/assets/dffe0b83-170e-4dda-88a3-3ed977543b03" />

<img width="512" height="288" alt="spider_tailed_horned_viper_1" src="https://github.com/user-attachments/assets/341f4d6a-38c2-42c5-b4ec-3a3efc1d38cc" />


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
      <img width="512" height="288" alt="savanna nightjar_2" src="https://github.com/user-attachments/assets/90022bb6-d16a-4584-9e1b-f7375b0edb6f" />
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
<img width="761" height="453" alt="image" src="https://github.com/user-attachments/assets/3c0c9fb5-2904-4c09-9ec2-2e11391cbba1" />


### 🔑 Key Hyperparameter Settings (Tips for Reproduction)
To achieve optimal performance on different datasets, we strongly recommend the following parameter configurations in your `config.yaml`:

* **SBP Dimension:** The dimension of Semantic Basis Primitives (SBP) is optimally set to **`384`**.
* **Theta ($\theta$) Value Adjustment:** The parameter $\theta$ in our alignment module is sensitive to dataset characteristics. We recommend:
  * For **MoCA** dataset: `theta = 0.458`
  * For **YUV** dataset: `theta = 0.158`
*(Note: In future work, $\theta$ can be extended as a learnable parameter rather than a fixed scalar.)*

---

## ⚙️ Getting Started

### Prerequisites
```bash
git clone [https://github.com/yourusername/YourProject.git](https://github.com/yourusername/YourProject.git)
cd YourProject
pip install -r requirements.txt
