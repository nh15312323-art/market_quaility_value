# Market Screening Specification

## 1. 목적

시장 전체 종목을 매일 자동으로 스크리닝하여 투자 후보 종목을 빠르게 발견하기 위한 기능이다.

Market Screening은 최종 투자 의사결정 시스템이 아니라 **Research / Discovery Engine**이다.

투자 철학은 다음과 같다.

> Momentum으로 후보를 발견하고, Quality + Growth + Valuation + Business Analysis를 통해 최종 투자 여부를 판단한다.

따라서 시장 스크리닝 단계에서는 특정 종목의 투자 적합성을 임의의 종합점수로 평가하지 않는다.

---

## 2. 기본 원칙

### 2.1 독립적인 Top 20 제공

각 지표별로 독립적인 Top 20 목록을 제공한다.

- Trading Value Z10 Top 20
- Trading Value Z20 Top 20
- 1D Return Top 20
- 5D Return Top 20
- 10D Return Top 20
- 20D Return Top 20
- 60D Return Top 20
- 120D Return Top 20
- Weighted Momentum Top 20
- KOSPI Relative Strength 20D Top 20
- KOSPI Relative Strength 60D Top 20
- KOSPI Relative Strength 120D Top 20

52주/3년/5년/10년 최고가 종목은 조건을 충족하는 전체 종목을 제공한다.

### 2.2 종합점수 사용 금지

V1에서는 임의의 0~100점 Composite Score 또는 Attention Score를 만들지 않는다.

각 지표를 독립적으로 보여주고 투자자가 후보를 발견하도록 한다.

향후 충분한 과거 데이터가 축적되면 백테스트를 통해 통계적으로 검증된 Composite Factor를 별도로 개발할 수 있다.

---

# 3. Universe

## 3.1 대상 시장

- KOSPI
- KOSDAQ

## 3.2 시가총액 기준

기준일 현재 시가총액이 500억원 이상인 종목만 포함한다.

```text
Market Cap >= KRW 50 billion
