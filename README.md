# Cybersecurity Anomaly Detection Projects

## Overview

This repository presents a structured anomaly detection pipeline for identifying suspicious login behavior in authentication logs. The project explores and compares statistical methods and unsupervised machine learning techniques to detect abnormal user activity patterns.

The objective is to evaluate how different approaches perform in detecting login anomalies such as brute-force attempts, burst failures, and unusual behavioral deviations.

## Problem Statement

Authentication systems generate large volumes of login events. Detecting anomalous behavior within these logs is critical for preventing:

- Brute-force attacks
- Credential stuffing
- Account takeover attempts
- Suspicious behavioral deviations

Traditional rule-based detection may miss subtle patterns, while machine learning approaches may detect broader behavioral irregularities. This project evaluates both perspectives.

## Project Structure

The repository is organized into five progressive stages:

### 01 – Statistical Baseline Detection
- Z-score anomaly detection
- Interquartile Range (IQR) outlier detection
- Identifies users with statistically abnormal failure counts

### 02 – Brute-Force Window Detection
- Time-window based detection logic
- Flags burst login failures within short intervals
- Simulates real-world brute-force detection logic

### 03 – Risk Scoring Model
- Assigns severity scores based on failed attempts
- Prioritizes alerts for investigation
- Demonstrates rule-based risk modeling

### 04 – Isolation Forest Model
- Unsupervised anomaly detection
- Aggregates behavioral features:
  - Failed attempts
  - Unique IP usage
  - Active duration
- Identifies multi-dimensional behavioral anomalies

### 05 – Method Comparison Analysis
- Compares:
  - Z-score
  - IQR
  - Isolation Forest
- Evaluates detection consistency
- Highlights strengths and limitations of each approach

## Methodology

The pipeline follows this workflow:

1. Log ingestion and preprocessing
2. Feature engineering at user level
3. Statistical anomaly detection
4. Time-based pattern detection
5. Unsupervised ML modeling
6. Comparative evaluation

Each method operates under different assumptions:

| Method | Type | Strength |
|--------|------|----------|
| Z-Score | Statistical | Detects extreme deviations |
| IQR | Statistical | Robust to skewed distributions |
| Time Window | Rule-Based | Captures burst attack behavior |
| Isolation Forest | ML | Detects multi-feature anomalies |

## Key Findings

- Statistical methods effectively detect users with unusually high failure rates.
- Time-window detection captures burst behavior missed by simple thresholds.
- Isolation Forest detects anomalies across multiple behavioral dimensions.
- Hybrid detection strategies are more robust than single-method approaches.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn (Isolation Forest)

## Research Relevance

This project demonstrates applied anomaly detection techniques relevant to:

- AI-driven cybersecurity systems
- Unsupervised learning research
- Behavioral anomaly modeling
- Security analytics

The structured comparison of statistical and ML approaches highlights trade-offs between explainability and detection flexibility.

## Future Work

- Incorporate real-world datasets
- Add IP reputation scoring
- Implement supervised anomaly classification
- Deploy as real-time detection pipeline
- Evaluate precision/recall on labeled attack data

## Author

Nehrin Gani  
Cybersecurity & AI Research Enthusiast

