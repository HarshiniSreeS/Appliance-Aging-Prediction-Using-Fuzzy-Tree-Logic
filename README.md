# Appliance-Aging-Prediction-Using-Fuzzy-Tree-Logic
# FUZZY TREE BASED APPLIANCE AGING PREDICTOR
## For Washing Machine

### 22AIE114 - Introduction to Electrical and Electronics Engineering

### Team 17 (AIE-A)
- Prakeya S (CB.SC.U4AIE25042)
- S Harshini Sree (CB.SC.U4AIE25044)
- Thiyaanesh N R (CB.SC.U4AIE25055)
- Yuvanidhi R (CB.SC.U4AIE25062)

---

# Intelligent Appliance Health Monitoring

## Focus of this project
Developing a Fuzzy Tree–Based Appliance Aging & Health Estimator to classify washing machine as:
- Healthy
- Aging
- Near Failure

## Problem Statement
Modern electrical appliances gradually degrade over time due to:
- Continuous usage
- Component wear

Traditional monitoring methods rely heavily on:
- Hardware sensors
- Manual inspection

There is a need for a low-cost software method to estimate appliance health based on behavioral indicators.

Our project is a low-cost software-based solution.

---

# EXISTING METHODS

## Manual Inspection
Appliance condition is checked manually by technicians based on:
- Visible faults
- Abnormal behavior

## Scheduled Maintenance
Appliances are serviced at regular time intervals regardless of their actual condition.

## Machine Learning Based Prediction
Machine learning algorithms analyze large datasets to:
- Detect faults
- Predict equipment failure

## Limitations of Existing Methods
- Require expensive hardware sensors
- Need large datasets for training models
- Implementation and maintenance costs are high
- Systems can be complex for small-scale appliance monitoring

---

# Objective of the Project

Fuzzy Tree Logic is a decision tree structure that uses fuzzy logic rules to classify data based on uncertain or imprecise inputs.

## Objectives
- Develop a fuzzy tree–based system for estimating appliance health conditions
- Analyze appliance behavior using:
  - Power consumption increase
  - Startup delay
  - Harmonic distortion
  - Usage frequency
- Apply fuzzy tree logic techniques to handle uncertain and imprecise appliance data
- Classify appliance conditions into:
  - Healthy
  - Aging
  - Near Failure
- Demonstrate a software-based predictive maintenance approach for appliances

---

# Types of Fuzzy Tree Algorithms

Fuzzy logic handles uncertainty using linguistic rules, while fuzzy tree structures organize multiple fuzzy systems efficiently for complex decision or prediction tasks.

## Fuzzy Logic Types

### 1) Mamdani Fuzzy System
- Uses linguistic rules and fuzzy outputs
- Result is converted to a crisp value using defuzzification
- Easy to interpret
- Widely used in control systems

### 2) Sugeno (Takagi–Sugeno) Fuzzy System
- Rules produce mathematical functions as outputs instead of fuzzy sets
- Faster computation
- Better suited for:
  - Prediction
  - Optimization
  - Data-driven models

### 3) Tsukamoto Fuzzy System
- Each rule produces a crisp output using monotonic membership functions
- Final result obtained by weighted averaging
- Less commonly used

---

# Fuzzy Tree Structures

## 1) Hierarchical Fuzzy Tree
Multiple fuzzy systems arranged in layers where outputs of lower nodes become inputs to higher nodes.

Advantages:
- Reduces rule complexity
- Suitable for systems with many parameters

## 2) Parallel Fuzzy Tree
Several fuzzy systems operate independently on different inputs, and their outputs are combined to produce the final result.

## 3) Hybrid Fuzzy Tree
Combination of hierarchical and parallel structures, used for complex systems with many interacting factors.

---

# Proposed Methodology

## 1. Input Parameter Selection
- Power consumption increase (%)
- Startup delay (seconds)
- Harmonic distortion (%)
- Usage frequency (cycles/day)

## 2. Dataset Generation
A dataset representing appliance behavior is generated using simulated values for the selected parameters.

## 3. Fuzzification
Crisp input values are converted into fuzzy membership values using triangular membership functions:
- Low
- Medium
- High

## 4. Fuzzy Rule Evaluation
A set of IF–THEN fuzzy rules is applied to analyze appliance conditions based on input parameters.

## 5. Fuzzy Decision Tree Logic
The fuzzy rules are organized in a decision tree structure to determine appliance health.

## 6. Defuzzification
The fuzzy output is converted into a crisp value representing appliance health.

## 7. Health Classification
The system classifies appliance condition as:
- Healthy
- Aging
- Near Failure

---

# FUZZY INFERENCE ARCHITECTURE

## FIS1
Inputs:
- Power
- Startup Delay

Output:
- Electrical Stress

## FIS2
Inputs:
- Harmonics
- Usage

Output:
- Thermal Stress

## FIS3
Inputs:
- Electrical Stress
- Thermal Stress

Output:
- Final Appliance Health Condition

---

# MATHEMATICAL MODEL

## Define Input Variables

Let:
- P = Power (Watts)
- S = Startup delay (seconds)
- H = Harmonic distortion (%)
- U = Usage frequency (cycles/day)

### Usage Frequency Formula
U = Total usage time per day / Time for one washing cycle

## Intermediate Outputs
- ES = Electrical Stress
- TS = Thermal Stress

## Output
- HS = Health Score

:contentReference[oaicite:0]{index=0}

:contentReference[oaicite:1]{index=1}

Where:
- f is the entire fuzzy decision system

---

# Fuzzification

Convert crisp input values into membership values between 0 and 1.

## Triangular Membership Function

:contentReference[oaicite:2]{index=2}

Where:
- x = input value
- a, b, c = triangle points
- μ(x) = membership value

---

# Tree Structure

## FIS1
Inputs:
- Power
- Startup Delay

Output:
- Electrical Stress

## FIS2
Inputs:
- Harmonics
- Usage

Output:
- Thermal Stress

## FIS3
Inputs:
- Electrical Stress
- Thermal Stress

Output:
- Final Health Score

---

# Real-Time Washing Machine Values

- P = 750W
- S = 2.5 sec
- H = 4.5%
- U = 2 cycles/day

---

# Fuzzify Power Increase

## Power Fuzzy Sets
- LOW → (200, 400, 600)
- MEDIUM → (500, 750, 1000)
- HIGH → (900, 1400, 2000)

For:
- P = 750W

Medium membership:

:contentReference[oaicite:3]{index=3}

---

# Fuzzify Startup Delay

## Startup Delay Fuzzy Sets
- FAST → (0,1,2)
- NORMAL → (1.5,3,5)
- SLOW → (4,6,8)

For:
- S = 2.5 sec

:contentReference[oaicite:4]{index=4}

---

# Fuzzify Harmonics

## Harmonics Fuzzy Sets
- LOW → (0,2,4)
- MEDIUM → (3,5,7)
- HIGH → (6,10,15)

For:
- H = 4.5%

:contentReference[oaicite:5]{index=5}

---

# Fuzzify Usage Frequency

## Usage Frequency Fuzzy Sets
- LIGHT → (0,1,2)
- MODERATE → (1,3,5)
- HEAVY → (4,6,8)

Cycles per day:

:contentReference[oaicite:6]{index=6}

Membership:

:contentReference[oaicite:7]{index=7}

---

# FIS1 : Electrical Stress Calculation

## Rule ES1
IF Power = High  
AND Startup Delay = Slow  
THEN ES = Severe

:contentReference[oaicite:8]{index=8}

## Rule ES2
IF Power = Medium  
AND Startup Delay = Normal  
THEN ES = Moderate

:contentReference[oaicite:9]{index=9}

## Rule ES3
IF Power = Low  
AND Startup Delay = Fast  
THEN ES = Low

:contentReference[oaicite:10]{index=10}

## Electrical Stress Defuzzification

:contentReference[oaicite:11]{index=11}

---

# FIS2 : Thermal Stress Calculation

## Rule TS1
IF Harmonics = High  
AND Usage = Heavy  
THEN TS = Severe

:contentReference[oaicite:12]{index=12}

## Rule TS2
IF Harmonics = Medium  
AND Usage = Moderate  
THEN TS = Moderate

:contentReference[oaicite:13]{index=13}

## Rule TS3
IF Harmonics = Low  
AND Usage = Light  
THEN TS = Low

:contentReference[oaicite:14]{index=14}

## Thermal Stress Defuzzification

:contentReference[oaicite:15]{index=15}

---

# FIS3 : Final Health Score

## Rule HS1
IF ES = Low  
AND TS = Low  
THEN Health = Healthy

:contentReference[oaicite:16]{index=16}

## Rule HS2
IF ES = Moderate  
AND TS = Moderate  
THEN Health = Aging

:contentReference[oaicite:17]{index=17}

## Rule HS3
IF ES = Severe  
OR TS = Severe  
THEN Health = Near Failure

:contentReference[oaicite:18]{index=18}

---

# Defuzzification

## Assign Output Scores

| Condition | Score |
|---|---|
| Healthy | 90 |
| Aging | 60 |
| Near Failure | 30 |

## Weighted Average

:contentReference[oaicite:19]{index=19}

:contentReference[oaicite:20]{index=20}

## Final Prediction
- Washing Machine Condition = Aging
- Final Health Score = 60

---

# RESULTS

- Development of a fuzzy tree-based model for predicting appliance health conditions
- Successful analysis of appliance behavior using:
  - Power consumption increase
  - Startup delay
  - Harmonic distortion
  - Usage frequency
- Accurate classification of appliance conditions into:
  - Healthy
  - Aging
  - Near Failure
- Demonstration of how fuzzy logic can handle uncertain and imprecise appliance data
- A software-based predictive maintenance approach that can help identify potential appliance failures early

## Code Repository
https://github.com/HarshiniSreeS/Appliance-Aging-Prediction-Using-Fuzzy-Tree-Logic

---

# REFERENCES

1. Hung-Lu Wang,  
“Reliability Evaluation of Household Appliance Protection System Based on Fuzzy Fault Tree Analysis,”  
2015 12th International Conference on Fuzzy Systems and Knowledge Discovery (FSKD), pp. 564–569, 2015.

2. S. R. Patil, P. R. Kumar,  
Smart Washing Machine Monitoring System Using IoT and Fuzzy Logic, 2021.

3. R. Kumar, S. Mishra,  
Condition Monitoring of Household Appliances Using Fuzzy Inference Systems, Wiley, 2019.

4. C. C. Lee,  
“Fuzzy Logic in Control Systems: Fuzzy Logic Controller – Part I,”  
IEEE Transactions on Systems, Man, and Cybernetics, vol. 20, no. 2, pp. 404–418, 1990.

5. L. X. Wang and J. M. Mendel,  
“Generating Fuzzy Rules by Learning from Examples,”  
IEEE Transactions on Systems, Man, and Cybernetics, vol. 22, no. 6, pp. 1414–1427, 1992.

6. George J. Klir and Bo Yuan,  
Fuzzy Sets and Fuzzy Logic: Theory and Applications, Prentice Hall, 1995.

---

# THANK YOU
