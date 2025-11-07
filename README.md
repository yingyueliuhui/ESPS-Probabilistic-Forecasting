# Electricity-Spot-Price-Spreads-Probabilistic-Forecasting

## Shanxi Power Market Time Series Dataset
## Overview
This dataset contains comprehensive time series data from the Shanxi provincial electricity market, spanning from January 1, 2024 to April 7, 2025 with 15-minute temporal resolution. The dataset is specifically designed for power market forecasting, price prediction, and energy trading analysis tasks.
## Dataset Structure
- **Temporal Resolution**: 15-minute intervals (96 data points per day)
- **Time Period**: January 1, 2024 - April 7, 2025
- **Total Duration**: ~463 days of high-frequency market data
## Data Partitioning
The dataset is strategically divided into three subsets:
- **Training Set**: Full year 2024 data (35,040 data points)
- **Validation Set**: January-February 2025 (6,960 data points)  
- **Test Set**: March 1 - April 7, 2025 (4,560 data points)
## Key Features
### Time Features
- Cyclically encoded using sine/cosine transformations to preserve temporal patterns
- Captures daily and weekly periodicity in power market behavior
### Market Variables
The dataset includes 20 core power market indicators:
#### Core Market Metrics
- **CEV_DA/CEV_DI**: Provincial cleared electricity volume (Day-ahead/Intra-day)
- **UCP_DA/UCP_DI**: Unified clearing price (Day-ahead/Intra-day, post-regulation)
- **UDEV_DA**: User declared electricity volume (Day-ahead)
#### Supply & Demand Indicators
- **TBS_DA/TBS_DI**: Thermal power bidding space (Day-ahead/Intra-day)
- **PDL_DA/PDL_DI**: Provincial dispatching load (Day-ahead/Intra-day)
- **SDR_DA/SDR_DI**: Supply-demand ratio (Day-ahead/Intra-day)
- **TLP_DA/TLP_DI**: Tie-line plan (Day-ahead/Intra-day)
#### Renewable Energy Metrics
- **NEL_DA/NEL_DI**: New energy load (Day-ahead/Intra-day)
- **WPO_DA/WPO_DI**: Wind power output (Day-ahead/Intra-day)
- **PVO_DA/PVO_DI**: Photovoltaic power output (Day-ahead/Intra-day)
#### Generation Capacity
- **HO_DA/HO_DI**: Hydropower output (Day-ahead/Intra-day)
- **NMUO_DA/NMUO_DI**: Non-marketized unit output (Day-ahead/Intra-day)
- **OLUC_DA/OLUC_DI**: On-line unit capacity (Day-ahead/Intra-day)
## Data Processing
- **Normalization**: All non-time features scaled to [0,1] range using standard scaling
- **Sliding Window**: Configurable window sizes for sequential modeling
  - Training: 1-step iteration for sequential learning
  - Validation/Test: 96-step windows (24-hour periods) for multi-step forecasting
## Applications
This dataset is ideal for:
- Short-term power price forecasting
- Load prediction and demand forecasting
- Renewable energy integration studies
- Market arbitrage strategy development
- Time series analysis and machine learning research
## Market Context
Aligned with standard electricity market trading intervals, the 15-minute granularity supports real-time decision-making applications and reflects the dynamic nature of modern power markets with increasing renewable energy penetration.
## Technical Specifications
- **Format**: Time-ordered sequential data
- **Feature Encoding**: Cyclic encoding for temporal features
- **Missing Data**: Handled with appropriate imputation techniques
- **Quality Control**: Validated against market trading intervals and operational constraints
This dataset provides researchers and practitioners with a comprehensive, high-quality resource for developing and testing power market forecasting models and understanding the complex dynamics of modern electricity markets.

--------------------------------
以上内容由AI生成，仅供参考和借鉴
