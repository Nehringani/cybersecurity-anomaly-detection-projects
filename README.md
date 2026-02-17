Cybersecurity Anomaly Detection Projects
A collection of cybersecurity-focused anomaly detection and intrusion detection projects comparing statistical methods and unsupervised machine learning approaches for detecting and analyzing suspicious behavior in authentication and network traffic logs.

Overview
This repository presents a structured progression of anomaly detection and intrusion detection projects focused on identifying suspicious behavior in both authentication logs and network traffic data.

The objective is to evaluate how different detection strategies perform in identifying:

Brute-force login attempts
Burst failures
Behavioral anomalies
Abnormal network traffic patterns

Intrusion-like activity
The projects evolve from basic statistical detection to machine learning-based anomaly detection and finally to a research-style evaluation study.

Problem Statement
Modern systems generate large volumes of authentication and network traffic logs. Detecting malicious behavior within this data is critical for preventing:

Brute-force attacks
Credential stuffing
Account takeover attempts
Privilege escalation
Data exfiltration

Suspicious network sessions
Traditional rule-based detection methods may miss subtle behavioral deviations, while machine learning models can detect broader multi-feature anomalies. This repository explores both approaches and evaluates their effectiveness.

Project Structure
The repository is organized into progressive stages:


01 – Statistical Baseline Detection
Z-score anomaly detection
Interquartile Range (IQR) outlier detection
Identifies users with statistically abnormal failure counts
Demonstrates basic threshold-based anomaly detection


02 – Brute-Force Window Detection
Time-window based detection logic
Flags burst login failures within short intervals
Simulates real-world brute-force detection behavior
Introduces rule-based detection concepts


03 – Risk Scoring Model
Assigns severity scores based on failed attempts
Prioritizes alerts for investigation
Demonstrates simple risk modeling logic
Bridges rule-based detection and behavioral assessment


04 – Isolation Forest Model (Authentication Logs)
Unsupervised anomaly detection
Aggregates behavioral features:
Failed attempts
Unique IP usage
Active duration
Identifies multi-dimensional behavioral anomalies
Demonstrates ML-based anomaly detection on login data


05 – Method Comparison Analysis
Compares:
Z-score
IQR
Isolation Forest
Evaluates detection consistency
Highlights strengths and limitations of each approach
Introduces analytical comparison methodology


06 – Network Traffic Anomaly Detection
Simulated network traffic dataset

Features analyzed:
Packet size
Connection duration
Bytes transferred
Applied Isolation Forest to detect abnormal traffic patterns
Visualized separation between normal and anomalous sessions
Extends anomaly detection beyond authentication logs


07 – Log-Based Intrusion Detection System
Simulated intrusion-like authentication behavior
Engineered behavioral indicators such as:
Failed login attempts
Abnormal login timing
User-level activity patterns
Combined rule-based logic with ML-based anomaly detection
Demonstrates layered detection design similar to hybrid IDS systems


08 – Research-Style Evaluation Study
Introduced labeled anomaly data for controlled evaluation
Compared:

Z-Score statistical detection
Isolation Forest predictions
Measured:
Precision
Recall
Confusion matrix
Demonstrated limitations of simple statistical methods
Highlighted strengths of unsupervised ML approaches

Methodology
The extended detection pipeline follows this workflow:

Log ingestion and preprocessing
Feature engineering (user-level and network-level)
Statistical anomaly detection (Z-score, IQR)
Time-based pattern detection
Unsupervised machine learning modeling (Isolation Forest)
Network-level anomaly simulation
Hybrid intrusion detection modeling
Research-style evaluation using labeled ground truth

Each method operates under different assumptions:

Method	Type	Strength
Z-Score	Statistical	Detects extreme deviations
IQR	Statistical	Robust to skewed distributions
Time Window	Rule-Based	Captures burst attack behavior
Isolation Forest	ML	Detects multi-feature anomalies
Hybrid Detection	Rule + ML	Layered detection capability

Key Findings
Statistical methods effectively detect extreme deviations but may fail in small or skewed datasets.
Time-window detection captures burst behavior missed by simple thresholds.
Isolation Forest detects anomalies across multiple behavioral dimensions.
Network-level modeling extends detection beyond authentication logs.
Z-score thresholding may fail when anomalies influence distribution statistics.
Unsupervised machine learning provides more flexible detection in evolving environments.
Hybrid detection approaches combining rules and ML improve robustness.

Technologies Used
Python
Pandas
NumPy
Matplotlib
Scikit-learn (Isolation Forest)
Scipy (Z-score computation)

Research Relevance
This repository demonstrates applied anomaly detection techniques relevant to:

AI-driven cybersecurity systems
Unsupervised learning research
Behavioral anomaly modeling
Intrusion detection system design
Security analytics

The later projects transition from practical anomaly simulation to structured research evaluation, aligning the repository with applied AI cybersecurity research practices.

Future Work
Incorporate real-world cybersecurity datasets (e.g., CICIDS, UNSW-NB15)
Compare additional anomaly detection algorithms
Introduce deep learning-based intrusion detection
Evaluate models using larger labeled datasets
Deploy detection logic into a real-time pipeline simulation

Author
Nehrin Gani
Cybersecurity & AI Research Enthusiast

