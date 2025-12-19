# Project 1: Principal Component Analysis (PCA)

본 프로젝트는 **차원 축소(Dimensionality Reduction)** 기법인  
**Principal Component Analysis (PCA)**를 직접 구현하고 실험하는 것을 목표로 합니다.  
이 프로젝트는 이후 **Autoencoder(AE)**와 **Variational Autoencoder(VAE)**로 확장되는  
representation learning 프로젝트의 출발점입니다.

---

## 📌 Project Overview

고차원 데이터는 계산 비용이 크고, 노이즈에 민감하며, 시각화가 어렵다는 문제를 가집니다.  
PCA는 데이터의 분산을 최대한 보존하는 방향으로 새로운 저차원 표현을 찾는  
대표적인 **선형 차원 축소 기법**입니다.

본 프로젝트에서는 PCA의 수학적 원리를 기반으로:
- 주성분(principal components)의 의미를 이해하고
- 차원 축소 전후의 데이터 표현을 비교하며
- 재구성(reconstruction) 성능을 분석합니다.

---

## 🔍 Methodology

### 1. Data Preprocessing
- 입력 데이터를 평균 0으로 정규화(mean centering)
- 공분산 행렬(covariance matrix) 계산

### 2. Eigen Decomposition
- 공분산 행렬의 eigenvalue / eigenvector 계산
- 가장 큰 eigenvalue를 가지는 방향을 principal component로 선택

### 3. Dimensionality Reduction
- 상위 \(k\)개의 principal components 선택
- 원본 데이터를 저차원 subspace로 projection

### 4. Reconstruction
- 저차원 표현으로부터 원본 공간으로 복원
- 차원 수에 따른 reconstruction quality 비교

---

## 📊 Experiments

- 서로 다른 principal component 개수에 따른:
  - 데이터 분산 보존 정도
  - 재구성 결과 비교
- 저차원 공간에서의 데이터 분포 시각화
- 차원 축소의 효과와 한계 분석

---

## 🛠 Implementation Details

- **Language:** Python  
- **Environment:** Jupyter Notebook  
- **Libraries:**
  - NumPy
  - Matplotlib
- **Implementation:**
  - PCA를 라이브러리 호출이 아닌 수식 기반으로 구현
  - Eigen decomposition을 통해 직접 주성분 계산

---

## 🎯 Key Learning Outcomes

- PCA의 수학적 의미와 직관 이해
- 분산 최대화 관점에서의 차원 축소 원리
- 차원 수 선택이 표현력에 미치는 영향
- 선형 차원 축소 기법의 한계 인식
- 이후 AE / VAE로 확장되는 representation learning의 기초 이해

---

## 📌 Notes

- 본 프로젝트는 **교육 목적의 실습 과제**입니다.
- PCA는 선형 기법이므로 복잡한 비선형 구조를 완전히 표현하지는 못합니다.
- 이러한 한계는 이후 프로젝트(Autoencoder, Variational Autoencoder)에서 다룹니다.

---

## ✨ Summary

이 프로젝트는  
> **“데이터를 더 적은 차원으로 표현한다는 것이 무엇을 의미하는가?”**  

라는 질문에 답하기 위한 첫 단계입니다.  
PCA를 통해 차원 축소의 기본 개념을 이해하고,  
딥러닝 기반 representation learning으로 나아가기 위한 기반을 마련합니다.
