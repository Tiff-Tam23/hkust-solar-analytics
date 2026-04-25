# 🌞 Optimizing Solar PV Performance at HKUST Using 3-Year High-Resolution Data

---

## 📖 Introduction

This project analyzes the performance of rooftop photovoltaic (PV) systems at The Hong Kong University of Science and Technology (HKUST) using a high-resolution dataset spanning three years (2021–2023). The goal is to evaluate system efficiency, detect anomalies, and recommend actionable improvements for solar energy optimization.

The analysis integrates environmental factors, statistical anomaly detection, and cross-location benchmarking to distinguish between weather-driven variability and hardware-related inefficiencies.

---

## 📚 Data Sources

This project is based on publicly available datasets and research:

**Article**:
A high-resolution three-year dataset supporting rooftop photovoltaics (PV) generation analytics)
https://www.nature.com/articles/s41597-025-04397-y#Sec8

**Dataset (Dryad Repository)**:
https://datadryad.org/dataset/doi:10.5061/dryad.m37pvmd99

These sources provide detailed PV generation, irradiance, rainfall, and environmental data used throughout the analysis.

---

## 🎯 Objectives
### Primary Goal

To provide a comprehensive understanding of the HKUST solar panel system and generate actionable recommendations for optimization.

### Specific Objectives
- Visual Insight: Build a diagnostic dashboard integrating multi-source data
- Event-Based Detection: Identify zero-output and abnormal performance days
- Environmental Correlation: Separate weather effects from hardware issues
- Cross-Location Benchmarking: Rank locations using statistical comparisons (Z-score)


---

## 🧠 Methodology
### 1. Event-Based Detection (2σ Rule)

Daily energy output is categorized using statistical thresholds:
- **Zero Day**: Near-zero output → possible system failure
- **Down Day**: Significantly below expected → potential issue
- **Normal Day***: Within expected range
- **Up Day**: Above expected performance

Formula: 

**Monthly Average (μ) ± 2σ**


This approach adapts to seasonal variations and detects true anomalies.


### 2. Environmental Correlation

Key influencing factors:

- **Irradiance**: Strong positive correlation  
- **Temperature**: Optimal range 22–28°C  
- **Rainfall**: Negative impact but cleaning effect post-rain

Weather thresholds:

- Low irradiance (<85% median)
- High rainfall (>130% median)

Used to classify:

- 🌧️ Weather-driven anomalies (~80%)
- ⚙️ Hardware-driven anomalies (~20%)


### 3. Cross-Location Benchmarking
- Z-score used to compare performance across locations
- Metrics:
   - Normal+ % (Good/Normal performance rate)
   - Average Z-score

