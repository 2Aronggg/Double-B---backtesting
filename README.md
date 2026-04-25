# Double-B: AI-Driven Quantitative Research & Backtesting

> **Quantitative Research Framework for Market Alpha Discovery**
> 
> 본 프로젝트는 금융 시장의 비효율성을 탐색하고 머신러닝 모델과 통계적 기법을 결합하여 데이터 기반의 투자 전략을 도출하는 퀀트 리서치 파이프라인이다.

---

## Overview
Double-B는 데이터 수집부터 피처 엔지니어링, 모델 학습, 그리고 전략 백테스팅과 시각화 대시보드까지 이어지는 End-to-End 리서치 시스템이다.

* **Alpha Discovery:** 다변량 데이터 분석을 통한 유의미한 투자 신호 포착
* **Systematic Backtesting:** 생존 편향 및 룩어헤드 편향을 배제한 엄격한 성과 검증
* **Data Visualization:** 리서치 결과를 분석하기 위한 대시보드 환경 제공

---

## Tech Stack
* **Language:** Python 3.9+
* **Data Analysis:** Pandas, NumPy, SciPy, Statsmodels
* **Machine Learning:** PyTorch, XGBoost, Scikit-learn
* **Visualization:** Plotly, Streamlit, Matplotlib
* **Database:** SQLite / PostgreSQL

---

## Methodology
본 프로젝트는 통계적 유의성과 리스크 관리에 중점을 둔다.

### 1. Factor Engineering
기술적 지표 분석뿐만 아니라 통계적 모멘텀 및 변동성 클러스터링을 분석하여 독립적인 알파 팩터를 추출한다.

### 2. Deep Learning Model
시계열 데이터의 비선형적 특성을 파악하기 위해 LSTM 또는 Transformer 아키텍처를 활용하여 자산 수익률의 방향성을 예측한다.

### 3. Portfolio Optimization
$$Maximize \ Sharpe \ Ratio = \frac{E[R_p - R_f]}{\sigma_p}$$
* **Risk Management:** MDD(Maximum Drawdown) 통제를 위한 동적 자산 배분 전략을 적용한다.
* **Position Sizing:** 켈리 공식 및 리스크 패리티 기반의 포지션 최적화를 수행한다.

---

## Research Workflow
1. **Data Ingestion:** 금융 데이터 API를 활용한 OHLCV 및 대안 데이터 수집
2. **Preprocessing:** 이상치 처리, Scaling 및 시계열 데이터의 정상성 확보
3. **Backtesting:** 거래 수수료, 슬리피지 등을 반영한 현실적인 시뮬레이션 시행
4. **Analysis:** Sharpe Ratio, Sortino Ratio, Information Ratio 등 성과 지표 산출

---

## Dashboard Preview
대시보드를 통해 전략별 수익률 곡선 및 리스크 지표를 실시간으로 모니터링할 수 있다. 
`streamlit run app.py` 명령어를 사용하여 로컬 리포트 환경을 구동한다.

---

## Quick Start
```bash
# 1. Repository Clone
git clone [https://github.com/your-username/Double-B.git](https://github.com/your-username/Double-B.git)

# 2. Dependency Install
pip install -r requirements.txt

# 3. Execution
python main.py
