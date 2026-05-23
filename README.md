# CCTV-Aanlysis
# 서울시 자치구별 CCTV 현황 분석

서울시 25개 자치구의 CCTV 설치 현황과 인구 데이터를 결합해 구별 CCTV 분포 및 인구 대비 설치 비율을 분석한 프로젝트입니다.

---

## 사용 데이터

| 파일명 | 출처 | 내용 |
|---|---|---|
| `CCTV_in_Seoul.csv` | 서울 열린데이터광장 | 자치구별 연도별 CCTV 설치 수 (2013년 이전 ~ 2016년) |
| `population_in_Seoul.xlsx` | 서울 열린데이터광장 | 자치구별 인구수, 한국인/외국인/고령자 수 |

---

## 분석 내용

**데이터 전처리**
- 컬럼명 정리 및 불필요한 행 제거
- 두 데이터셋을 자치구 기준으로 병합

**탐색적 데이터 분석 (EDA)**
- CCTV 총 설치 수 기준 상위/하위 자치구 확인
- 2014~2016년 최근 3년간 CCTV 증가율 계산

**시각화**
- 자치구별 CCTV 설치 수 가로 막대 차트
- 인구수 대비 CCTV 설치 비율 산점도 (선형회귀선 포함)
- 인구 대비 CCTV 수가 많은 구 / 적은 구 비교

---

## 주요 결과

- CCTV 설치 수 1위는 **강남구(3,238대)**, 최하위는 **도봉구(825대)**
- 인구수와 CCTV 설치 수 사이에는 양의 상관관계가 존재하나, 구별 편차가 큼
- 인구 대비 CCTV가 과소 설치된 구와 과다 설치된 구를 오차 기반으로 시각적으로 구분

---

## 사용 기술

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat)

---

## 실행 방법

```bash
jupyter notebook CCTV_Seoul.ipynb
```

> 데이터 파일(`CCTV_in_Seoul.csv`, `population_in_Seoul.xlsx`)을 `data/` 폴더에 넣고 실행하세요.
