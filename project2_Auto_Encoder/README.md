# Project 2: Autoencoder (AE)

본 프로젝트는 **Autoencoder (AE)**를 활용하여  
데이터의 **비선형 차원 축소 및 representation learning**을 수행하는 것을 목표로 합니다.  
이는 Project 1의 **PCA(선형 차원 축소)**에서 한 단계 확장된 접근으로,  
신경망을 통해 더 복잡한 데이터 구조를 학습합니다.

---

## 📌 Project Overview

Autoencoder는 입력 데이터를 저차원 latent space로 압축한 뒤,  
다시 원본 공간으로 복원하도록 학습되는 **unsupervised neural network**입니다.  
PCA와 달리, AE는 **비선형 함수**를 사용하여 데이터의 복잡한 구조를 표현할 수 있습니다.

본 프로젝트에서는:
- Encoder / Decoder 구조를 직접 설계하고
- Latent dimension 변화에 따른 표현력 차이를 분석하며
- PCA와 Autoencoder의 차이를 실험적으로 비교합니다.

---

## 🧠 Model Architecture

Autoencoder는 다음과 같은 구조로 구성됩니다:

- **Encoder**
  - 입력 데이터를 점진적으로 압축
  - 저차원 latent representation 생성

- **Latent Space**
  - 데이터의 핵심 특징을 담은 압축 표현
  - 차원 수를 조절하며 실험 수행

- **Decoder**
  - Latent representation으로부터 입력 데이터 복원

손실 함수로는 **reconstruction loss (MSE)**를 사용하여  
입력과 출력의 차이를 최소화하도록 학습합니다.

---

## 🔍 Methodology

1. 데이터 정규화 및 전처리  
2. Autoencoder 모델 정의 (fully-connected layers)  
3. Forward / Backward propagation을 통한 학습  
4. Reconstruction loss 기반 성능 평가  
5. Latent dimension 변화에 따른 결과 비교  

---

## 📊 Experiments

- Latent dimension 크기에 따른:
  - Reconstruction quality 변화
  - 정보 손실 정도 분석
- 원본 데이터와 재구성된 데이터 비교 시각화
- PCA 결과와 Autoencoder 결과의 차이 분석

---

## 🛠 Implementation Details

- **Language:** Python  
- **Environment:** Jupyter Notebook  
- **Libraries:**
  - PyTorch
  - NumPy
  - Matplotlib
- **Model Type:** Fully-connected Autoencoder
- **Training:** Unsupervised learning

---

## 🎯 Key Learning Outcomes

- PCA와 Autoencoder의 구조적 차이 이해
- 선형 vs. 비선형 차원 축소 기법 비교
- Neural network 기반 representation learning 개념 습득
- Latent space의 의미와 역할 이해
- Reconstruction loss를 통한 unsupervised 학습 경험

---

## 📌 Notes

- 본 프로젝트는 **교육 목적의 실습 과제**입니다.
- Autoencoder는 deterministic한 latent representation을 학습합니다.
- Latent space의 확률적 모델링은 다음 프로젝트(VAE)에서 다룹니다.

---

## ✨ Summary

이 프로젝트는  
> **“신경망은 어떻게 데이터를 압축하고 다시 복원할 수 있는가?”**  

라는 질문에 답하는 실험입니다.  
Autoencoder를 통해 PCA의 한계를 넘어,  
비선형 구조를 학습하는 representation learning의 가능성을 확인합니다.
