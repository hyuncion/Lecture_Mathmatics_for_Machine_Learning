# Lecture: Mathematics for Machine Learning
**PCA · Autoencoder · Variational Autoencoder**

본 저장소는 **표현 학습(Representation Learning)**을 주제로 수행한 3개의 프로젝트를 정리한 것입니다.  
각 프로젝트는 데이터의 저차원 표현을 학습하는 방법을 단계적으로 확장하며,

> **PCA → Autoencoder → Variational Autoencoder**

의 흐름을 통해  
선형 차원 축소에서 비선형·확률적 표현 학습까지 자연스럽게 이어집니다.

---

## 📌 Project Overview

고차원 데이터는 계산 비용이 크고 해석이 어려운 문제를 가집니다.  
Representation Learning은 데이터를 더 compact하고 의미 있는 형태로 표현하는 것을 목표로 합니다.

이 저장소의 프로젝트들은 다음 질문에 단계적으로 답합니다:

1. **PCA**  
   → 분산을 최대한 보존하는 선형 차원 축소란 무엇인가?

2. **Autoencoder (AE)**  
   → 신경망은 어떻게 비선형 구조를 학습하여 데이터를 압축할 수 있는가?

3. **Variational Autoencoder (VAE)**  
   → Latent space를 확률 분포로 모델링하면 무엇이 달라지는가?

---

## 📂 Projects

### 🔹 Project 1: Principal Component Analysis (PCA)
- 선형 차원 축소 기법
- 공분산 행렬 기반 eigen decomposition
- 분산 보존과 재구성(reconstruction) 분석
- AE/VAE의 baseline 역할

📁 `project1_pca/`

---

### 🔹 Project 2: Autoencoder (AE)
- Neural network 기반 비선형 차원 축소
- Encoder–Decoder 구조
- Reconstruction loss 기반 학습
- PCA와의 표현력 비교

📁 `project2_autoencoder/`

---

### 🔹 Project 3: Variational Autoencoder (VAE)
- 확률적 latent representation 학습
- Reparameterization Trick 적용
- Reconstruction loss + KL divergence
- Generative model로서의 특성 분석

📁 `project3_vae/`

---

## 🧠 Key Concepts

이 프로젝트 시리즈를 통해 다음 개념들을 학습하고 비교했습니다:

- Dimensionality Reduction
- Latent Space Representation
- Linear vs. Non-linear Models
- Deterministic vs. Probabilistic Encoding
- Generative Modeling
- Unsupervised Learning

---

## 🛠 Implementation Details

- **Language:** Python  
- **Environment:** Jupyter Notebook  
- **Libraries:**
  - NumPy
  - Matplotlib
  - PyTorch (AE, VAE)

모든 프로젝트는 **unsupervised learning** 설정에서 수행되었습니다.

---

## 🎯 Learning Objectives

이 시리즈의 학습 목표는 다음과 같습니다:

- 차원 축소 기법의 이론적 배경과 직관 이해
- PCA의 한계와 신경망 기반 접근의 장점 비교
- Latent space의 의미와 역할 이해
- 확률적 모델링이 representation에 미치는 영향 분석
- Representation learning의 단계적 발전 과정 체득

---

## 📌 Notes

- 본 프로젝트들은 **교육 목적의 실습 과제**입니다.
- 수식 기반 설명은 Jupyter Notebook에 포함되어 있으며,  
  GitHub README에서는 가독성을 위해 텍스트/코드 블록 형식으로 정리했습니다.
- 데이터셋과 하이퍼파라미터에 따라 결과는 달라질 수 있습니다.

---

## ✨ Summary

이 저장소는  
> **“데이터를 어떻게 더 잘 표현할 것인가?”**  

라는 질문에 대해,  
선형 기법(PCA)에서 시작해 비선형(AE), 확률적 모델(VAE)로 확장해 나가는  
**Representation Learning 학습 여정**을 담고 있습니다.

각 프로젝트는 독립적으로 이해 가능하면서도,  
함께 보았을 때 하나의 일관된 흐름을 이루도록 구성되어 있습니다.
