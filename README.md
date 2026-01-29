# Structural-Shifts-in-International-Crime_South-Korea

## Structural Shifts in International Crime in South Korea
### 대한민국 국제범죄의 구조적 변화 분석

### – 건수 기반 분석에서 구조·국면 분석으로의 확장 –

## 1. Overview

본 프로젝트는 대한민국 국제범죄의 변화를
"단순한 발생 건수나 개별 범죄 유형의 증감"이 아닌,
범죄 유형 간 **구성(composition)과 관계로 이루어진 구조(structure)**의 변화로 분석한다.

기존 국제범죄 분석은 주로 다음에 초점을 맞추어 왔다.

- 연도별 국제범죄 발생 건수 추이
- 특정 범죄 유형(마약, 사이버범죄 등)의 증가 여부
- 단기적 변동성에 대한 해석

그러나 이러한 접근은

“국제범죄 환경이 어떻게 재편되고 전환(regime shift)되는가”
를 설명하는 데 구조적 한계를 가진다.

이에 본 프로젝트는 동일한 원자료를 사용하되,
분석 관점을 건수 중심 → 구조 중심으로 전환하여
국제범죄의 장기적 구조 변화와 국면 전환을 데이터 기반으로 규명하는 것을 목표로 한다.

## 2. Research Motivation

국제범죄는 단일 범죄 유형의 문제가 아니라,
사회·기술·경제·국제 환경 변화에 따라
### 범죄 유형의 조합과 비중이 재구성되는 구조적 현상
으로 나타난다.

그러나 기존 접근은 다음과 같은 한계를 가진다.

1. 범죄 건수 증감 중심의 단편적 해석
2. 특정 범죄 유형에 대한 개별·분절적 분석
3. 장기적 관점에서의 구조 변화 설명 부족

본 프로젝트는 이러한 한계를 인식하고,
국제범죄를 **다변량 구조(multivariate structure)**로 재정의함으로써
범죄 환경의 **국면 전환(regime shift)**을 설명하는 것을 핵심 목표로 한다.

## 3. Data & Scope
### 3.1 Data Sources

### Primary (정량 분석용)

- 대한민국 경찰청 범죄통계

- 대검찰청 범죄백서

- 관세청 밀수·관세범 통계

### Secondary (정의·비교 참고)

- UNODC 국제범죄 유형 분류 체계

- 국제범죄 정의 관련 공공 문헌

### Exploratory (맥락 이해용)

- 공개 OSINT 리포트 및 정책 문헌
※ 정량 분석에는 사용하지 않음

### 3.2 Period Definition

Core Analysis Period: 2005–2023

- 공식 통계 확정치 기반

- 모든 구조적 결론은 해당 구간에 한해 도출

Exploratory Extension: 2024–2025

잠정·부분 공개 자료 포함

구조적 결론 도출 ❌

변화 방향성 관측에 한정

## 4. Analysis Pipeline
### Phase 1. Conventional Analysis

(Baseline & Limitation Identification)

- 국제범죄 전체 발생 건수 시계열

- 범죄 유형별 발생 건수 추이

- 범죄 유형별 구성비 변화

➡️ 기존 분석 방식의 설명력과 한계를 명확히 확인

## Phase 2. Structural Analysis

(Structure, Change Point, Regime)

- 국제범죄 구조 벡터화
(연도 × 범죄유형 구성비)

- 구조 변화 탐지 (Change Point Detection)

- 차원 축소 기반 구조 궤적 분석 (PCA)

- 국면(Regime) 분석 및 군집화

➡️ 국제범죄 환경의 구조적 전환 규명

## 5. Phase 1 Results — Conventional Analysis
### 5.1 Total Crime Trend

📌 [Figure 1 here: Total International Crime Count by Year](notebooks/figures/phase1_V1_total_trend.png)
📌 [Table 1 here: Total International Crime Count by Year](notebooks/figures/phase1_V1_total_trend_table.png)

X-axis: Year (2005–2023)
Y-axis: Total number of international crime cases

Interpretation

- 2014년 전후 뚜렷한 수준 변화(level shift)

- 2020년 팬데믹 시기 급감

- 이후 재상승 국면 진입

➡️ 총량만으로도 구조적 단절 가능성 시사

5.2 Category-level Trends

📌 [Figure 2 here: Category-level Count Trends](notebooks/figures/phase1_V2_category_trends.png)
📌 [Table 2 here: Category-level Count by Year]

X-axis: Year
Y-axis: Annual count by category

Interpretation

OTHER 범주가 절대적 비중 유지

FRAUD_FIN(국제 사기·금융범죄)의 구조적 증가

CYBER 범죄의 점진적 확대

5.3 Composition (Share) Analysis

📌 [Figure 3 here: Stacked Area Chart of Category Share] 
📌 [Table 3 here: Category Share by Year]

X-axis: Year
Y-axis: Share (sum = 1)

Interpretation

OTHER 비중 감소

FRAUD_FIN, CYBER의 상대적 중요성 증가

총량보다 ‘구성 변화’가 핵심 신호

6. Phase 2 Results — Structural Analysis
6.1 Structural Distance & Change Points

📌 [Table 4 here: Structural Distance Between Consecutive Years]
📌 [Table 5 here: Change Point Candidates]

Concept (직관적 설명)

각 연도는 “범죄 유형 구성비 벡터”

연도 간 거리 = 범죄 구조 차이

Key Finding

2018년, 2020년에서 구조 거리 급증

단순 변동 ❌ → 구조적 전환 시점

6.2 Regime Analysis

📌 [Table 6 here: Regime-wise Average Structure]

Regime 0: 전통적 국제범죄 구조

Regime 1: 금융·사이버 중심 구조

Regime 2: 과도기적·불안정 구조

➡️ 국제범죄 구조는 연속적 변화가 아닌 국면 전환

6.3 PCA-based Structural Space Analysis (중요)

📌 [Figure 7 here: PCA Trajectory of Crime Structure]
📌 [Figure 8 here: EXT Projection onto PCA Space]

PC1 (X-axis)

전통 범죄 ↔ 금융·사이버 범죄 축

구조 변화의 주된 방향

PC2 (Y-axis)

비주류 범죄 조합 및 내부 변동성

Interpretation

Regime 간 이동은 “점프(jump)” 형태

EXT(2024–2025)는 기존 Regime보다 더 진전된 위치

➡️ 과거 기준 대응의 한계 시사

7. Conclusion

국제범죄는 단순히 “늘었다/줄었다”의 문제가 아니라,
구조적으로 재편되고 국면이 전환되는 현상임이 확인되었다.

본 프로젝트는
국제범죄 분석을 건수 중심 접근에서 구조 중심 접근으로 확장하였으며,
정책·정보·치안 분야에서의 해석 프레임 전환 필요성을 제시한다.

8. Limitations & Future Work

원자료 비공개로 인한 완전 재현성 한계

국제 비교 분석의 제한적 적용

Future Work

국가 간 구조 비교

정책 개입 전·후 구조 변화 분석

조기 경보(Early Warning) 지표 개발

9. Use of AI

본 프로젝트에서는 AI 도구를 다음 목적에 한해 활용하였다.

분석 파이프라인 설계 보조

구조 분석 방법론 정리 및 문서화

코드 가독성 및 문서 구조 개선

모든 분석 판단과 해석은 연구자가 직접 수행하였다.
