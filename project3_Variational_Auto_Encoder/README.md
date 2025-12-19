# Project 3: Variational Autoencoder (VAE)

본 프로젝트는 **Variational Autoencoder (VAE)**를 구현하고 실험하여  
latent space를 **확률 분포(probabilistic representation)**로 모델링하는 것을 목표로 합니다.  
이는 Project 2의 **Autoencoder(AE)**에서 한 단계 확장된 접근으로,  
단순한 재구성을 넘어 **generative model**로서의 성질을 학습합니다.

---

## 📌 Project Overview

Autoencoder는 입력 데이터를 저차원 latent space로 압축하고 복원하는 데 초점을 두지만,  
latent representation은 deterministic하며 샘플링이 어렵다는 한계를 가집니다.  

VAE는 latent space를 **확률 분포(보통 Gaussian)**로 가정하고,  
데이터 분포를 학습함으로써 새로운 데이터를 생성할 수 있는  
**generative representation learning 모델**입니다.

본 프로젝트에서는:
- Encoder가 latent distribution의 파라미터를 학습하도록 설계하고
- Reparameterization Trick을 통해 학습 가능하게 만들며
- Reconstruction과 Regularization을 동시에 고려한 학습을 수행합니다.

---

## 🧠 Model Architecture

VAE는 다음과 같은 구조를 가집니다:

### Encoder
- 입력 데이터를 latent distribution의 파라미터로 매핑
- 출력: **mean (μ)**, **log-variance (log σ²)**

### Latent Space
- Gaussian distribution 기반 latent variable \(z\)
- Reparameterization Trick:
z = μ + σ · ε, ε ~ N(0, I)

### Decoder
- 샘플링된 latent variable로부터 입력 데이터 복원

---

## 🔍 Loss Function

VAE는 두 가지 손실 항을 동시에 최소화합니다:

1. **Reconstruction Loss**
   - 입력과 복원 결과의 차이 (MSE 또는 BCE)

2. **KL Divergence**
   - 학습된 latent distribution과 표준 정규분포 간의 거리
   - Latent space의 정규화 역할

전체 loss: L = L_recon + L_KL

---

## 📊 Experiments

- Latent dimension 변화에 따른:
  - Reconstruction quality 비교
  - Latent space 구조 분석
- Latent space에서 샘플링을 통한 **새로운 데이터 생성**
- AE와 VAE의 reconstruction 및 latent representation 비교
- Latent space 시각화 (2D projection)

---

## 🛠 Implementation Details

- **Language:** Python  
- **Environment:** Jupyter Notebook  
- **Libraries:**
  - PyTorch
  - NumPy
  - Matplotlib
- **Model Type:** Fully-connected Variational Autoencoder
- **Training:** Unsupervised learning

---

## 🎯 Key Learning Outcomes

- Deterministic AE와 probabilistic VAE의 차이 이해
- Latent space를 분포로 모델링하는 개념 습득
- Reparameterization Trick의 역할과 필요성 이해
- KL Divergence의 의미와 regularization 효과
- Generative model로서 VAE의 가능성 이해

---

## 📌 Notes

- 본 프로젝트는 **교육 목적의 실습 과제**입니다.
- VAE는 reconstruction 성능보다 latent space 구조 학습에 중점을 둡니다.
- Hyperparameter 설정(β, latent dim)에 따라 결과가 크게 달라질 수 있습니다.

---

## ✨ Summary

이 프로젝트는  
> **“latent representation을 확률적으로 모델링하면 무엇이 달라지는가?”**  

라는 질문에 답하기 위한 실험입니다.  
VAE를 통해 단순한 차원 축소를 넘어,  
**데이터 생성이 가능한 representation learning**의 개념을 이해합니다.
