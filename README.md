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

- 전기 및 가스 사용 데이터를 기반으로  
  **탄소 배출량의 시계열 패턴을 분석**
- SARIMA 모델을 활용하여  
  **2025~2028년 탄소 배출량을 예측**
- 분석 결과를 바탕으로  
  **탄소 절감 정책 및 전략 제안**

---

## 1. Project Overview

- **주제**: 에너지 사용량과 탄소 배출량 간 관계 분석
- **분석 대상**: 서울시 전기 및 가스 사용 데이터
- **문제 유형**: 시계열 분석(Time Series Forecasting)
- **핵심 목표**
  - 탄소 배출 패턴 분석
  - 시계열 모델 기반 미래 예측
  - 정책적 활용 가능 인사이트 도출

---

## 2. Data Description

- 전기 사용량 기반 탄소 배출량
- 가스 사용량 기반 탄소 배출량
- 월별 시계열 데이터 형태

> ※ 공공데이터 기반 프로젝트로, 원본 데이터는 현재 포함되어 있지 않습니다.

---

## 3. Problem Definition

- 에너지 사용 증가에 따른 탄소 배출 증가 문제
- 계절성 및 추세를 포함한 시계열 데이터 특성 존재
- 단순 분석이 아닌 **미래 예측 및 정책 활용 필요**

---

## 4. Data Analysis Process

### 1) 시계열 구조 분석
- 추세(Trend) 및 계절성(Seasonality) 확인
- 시각화를 통한 패턴 분석

### 2) 정상성 검정
- ADF Test
- KPSS Test

👉 시계열 모델 적용을 위한 전처리 수행

---

### 3) 모델링

- **SARIMA (Seasonal ARIMA)** 모델 적용
- ACF / PACF 기반 파라미터 설정
- 계절성 반영 모델링 수행

---

### 4) 시계열 예측

- 2025 ~ 2028년 탄소 배출량 예측
- 신뢰구간(Confidence Interval) 포함

---

## 5. 분석 결과

- 전기 및 가스 사용량은 **뚜렷한 계절성 패턴**을 보임
- 여름/겨울철 에너지 사용 증가 → 탄소 배출 증가
- 장기적으로 완만한 증가 추세 확인

---

## 6. 정책 제안 (Insight)

### 🚲 친환경 교통 확대
- 따릉이 이용 활성화
- 자동차 의존도 감소

### 🚗 전기차 보급 확대
- 내연기관 차량 대체
- 장기적 탄소 감축 효과 기대

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
├── assets/
│   └── (6조)_에너지 사용과 탄소 절감 방안.pptx
└── README.md
```

---

## 📄 프로젝트 자료

- 발표 자료: [(6조)_에너지 사용과 탄소 절감 방안](./assets/에너지%20사용과%20탄소%20절감%20방안%20.pdf)

---

## 🛠️ 사용 기술

- Python
- Time Series Analysis
- SARIMA
- ADF / KPSS Test
- Matplotlib

---

## ⚠️ 참고 사항

- 본 프로젝트는 발표자료 기반으로 정리되었습니다.
- 원본 데이터 및 일부 실행 파일은 현재 포함되어 있지 않습니다.
