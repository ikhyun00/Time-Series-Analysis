# Time-Series-Analysis
# ⚡ Energy Consumption & Carbon Emission Analysis

<div align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/TimeSeries-SARIMA-orange?style=for-the-badge">
  <img src="https://img.shields.io/badge/Statistics-ADF%20%7C%20KPSS-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/Visualization-Matplotlib-green?style=for-the-badge">
</div>

---

## 📖 프로젝트 주제
**서울시 에너지 사용량 기반 탄소 배출 분석 및 시계열 예측**

- 전기 및 가스 사용에 따른 온실가스 배출량을 기반으로  
  **탄소 배출량의 시계열 패턴을 분석**
- SARIMA 모델을 활용하여  
  **2025~2028년 탄소 배출량을 예측**
- 따릉이·전기차 보급량 예측을 바탕으로  
  **탄소 절감 효과를 정량화하고 전략 제안**

---

## 1. Project Overview

- **주제**: 에너지 사용량과 탄소 배출량 간 관계 분석
- **분석 대상**: 서울시 전기·가스 온실가스 배출량, 따릉이 이용횟수, 전기차 등록대수
- **문제 유형**: 시계열 분석(Time Series Forecasting)
- **핵심 목표**
  - 탄소 배출 패턴 분석
  - 시계열 모델 기반 미래 예측
  - 정책적 활용 가능 인사이트 도출

---

## 2. Data Description

- 전기 사용량 기반 탄소 배출량 (2018~2024 월별, tCO₂)
- 가스 사용량 기반 탄소 배출량 (2018~2024 월별, tCO₂)
- 따릉이 이용횟수 (2017 ~ 2024 월별), 전기차 등록대수 (2017 ~ 2022 월별)

> ※ 공공데이터 기반 프로젝트로, 전기·가스 배출량 원본 데이터(연도별 엑셀 14개)는 `Data/` 폴더에 포함되어 있습니다.

---

## 3. Problem Definition

- 에너지 사용 증가에 따른 탄소 배출 증가 문제
- 전기는 여름, 가스는 겨울에 최고치를 보이는 12개월 주기 계절성 존재
- 단순 분석이 아닌 **미래 예측 및 정책 활용 필요**

---

## 4. Data Analysis Process

### 1) 시계열 구조 분석
- 추세(Trend) 및 계절성(Seasonality) 확인
- ACF / PACF 시각화를 통한 패턴 분석

### 2) 정상성 검정
- ADF Test (귀무가설: 정상)
- KPSS Test (귀무가설: 정상)

👉 두 검정으로 교차 확인 후 1차 차분 및 계절 차분(12개월) 수행

---

### 3) 모델링

- **SARIMA (Seasonal ARIMA)** 모델 적용
- ACF / PACF 기반 후보 설정 후 auto_arima 및 AIC 기준 선택
- 전기: SARIMA(0,1,0)(0,1,2)₁₂ / 가스: SARIMA(0,1,0)(2,1,0)₁₂
- 따릉이: 로그 변환 후 SARIMA(0,1,1)(1,1,0)₁₂ / 전기차: ARIMA(0,2,2)
- Ljung-Box, Jarque-Bera 검정으로 잔차 진단

---

### 4) 시계열 예측

- 2025 ~ 2028년(48개월) 탄소 배출량 예측
- 신뢰구간(Confidence Interval) 포함

---

## 5. 분석 결과

- 전기 및 가스 사용량은 **뚜렷한 계절성 패턴**을 보임
- 여름철(전기)·겨울철(가스) 에너지 사용 증가 → 탄소 배출 증가
- 장기적으로 전기는 **증가 추세**, 가스는 **감소 추세** 확인

---

## 6. 정책 제안 (Insight)

### 🚲 친환경 교통 확대
- 따릉이 이용 활성화 (이용횟수 지속 증가 예측)
- 월별 CO₂ 절감량 = 예측 이용건수 × 평균 이동거리 3.16km × 0.232kg/km

### 🚗 전기차 보급 확대
- 내연기관 차량 대체
- 전기차 1대당 월 약 164.4kg CO₂ 절감 기대

### ⚡ 에너지 효율 개선
- 계절별 에너지 관리 전략 필요
- 피크 시간대 사용량 조절

---

## 7. Conclusion

- 에너지 사용 데이터만으로도  
  **탄소 배출 패턴 및 미래 예측이 가능함을 확인**
- 시계열 모델을 활용하여  
  **정책적 의사결정에 활용 가능한 인사이트 도출**
- 친환경 교통 및 에너지 정책이  
  탄소 절감에 핵심 역할 수행 가능

---

## 📁 프로젝트 구조

```bash
├── Data/
│   └── ghgEmissions_data*.xlsx
├── 에너지 사용과 탄소 절감 방안.pdf
└── README.md
```

---

## 📄 프로젝트 자료

- 보고서: [에너지 사용과 탄소 절감 방안](./에너지%20사용과%20탄소%20절감%20방안.pdf)

---

## 🛠️ 사용 기술

- Python
- Time Series Analysis
- SARIMA
- ADF / KPSS Test
- Ljung-Box / Jarque-Bera Test
- Matplotlib

---

## ⚠️ 참고 사항

- 본 프로젝트는 발표자료 기반으로 정리되었습니다.
- 분석 코드(노트북)는 현재 저장소에 포함되어 있지 않습니다.
