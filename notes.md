PHASE 1:  

Observation 1:
No missing values.

Observation 2:
Target classes are balanced.

Observation 3:
RAM seems strongly related to price_range.

Observation 4:
No duplicate rows. 

Found:
RAM has a strong positive relationship with price_range.

Meaning:
RAM is likely an important predictor.

Next step:
Verify using correlation and later feature importance.

Questions Section: 

Questions I want this dataset to answer

1. Does RAM affect price?

2. Does internal memory affect price?

3. Does battery matter?

4. Does screen resolution matter?

5. Is weight related to price?

6. Is 4G more common in expensive phones?

7. Is talk time important?

8. Which feature contributes the most?

9. Are there redundant features?

10. Can I engineer better features? 

| Priority | Feature              | Why first?                                |
| -------- | -------------------- | ----------------------------------------- |
| ⭐⭐⭐⭐⭐    | RAM                  | Biggest influence on smartphone price     | 
| ⭐⭐⭐⭐⭐    | battery_power        | Battery capacity is a major selling point |
| ⭐⭐⭐⭐     | int_memory           | Storage significantly impacts price       |
| ⭐⭐⭐⭐     | clock_speed          | CPU performance                           |
| ⭐⭐⭐⭐     | n_cores              | Processing capability                     |
| ⭐⭐⭐⭐     | px_height + px_width | Display quality                           |
| ⭐⭐⭐      | pc + fc              | Camera quality                            |
| ⭐⭐⭐      | mobile_wt            | Design characteristic                     |
| ⭐⭐⭐      | talk_time            | Battery performance                       |
| ⭐⭐       | sc_h + sc_w          | Physical screen size                      |
| ⭐⭐       | m_dep                | Phone thickness                           |
| ⭐        | Binary features      | Bluetooth, Wi-Fi, 4G, etc.                |



Performance
──────────────
RAM
Clock Speed
Number of Cores

Storage
──────────────
Internal Memory

Battery
──────────────
Battery Power
Talk Time

Display
──────────────
Pixel Height
Pixel Width
Screen Height
Screen Width

Camera
──────────────
Primary Camera
Front Camera

Connectivity
──────────────
Bluetooth
WiFi
3G
4G
Dual SIM

Design
──────────────
Mobile Weight
Mobile Depth
Touch Screen 

| Instead of...            | Use...                                     |
| ------------------------ | ------------------------------------------ |
| Peak value               | **Highest frequency**                      |
| Highest number of phones | **Highest concentration of phones**        |
| Spread throughout        | **Distributed across the entire range**    |
| Same everywhere          | **Approximately uniform**                  |
| One bar is high          | **A noticeable concentration is observed** |


## Feature Analysis 1: RAM 

# HISTOGRAM : n core 

plt.figure(figsize=(8,5))

sns.histplot(
    df["n_cores"],
    bins=8,
    color="orange"
)

plt.title("Distribution of Number of CPU Cores")
plt.xlabel("Number of Cores")
plt.ylabel("Number of Phones")

plt.show() 

## Observations  

# Phase B — Compare with Target (Mobile Weight vs Price Range) 

## Business Question
Does mobile weight influence the mobile phone price range?

## Hypothesis 

# BOX PLOT : N Cores VS Price Range 

plt.figure(figsize=(8,5)) 

sns.boxplot( 
    data=df, 
    x=("price_range"),  
    y=("n_cores") 
) 

plt.title("") 
plt.xlabel("Price Range") 
plt.ylabel("N Cores") 

plt.show()    

# 

# Phase 1: Data Understanding
- Dataset overview
- Shape
- Data types
- Statistical summary

# Phase 2: Data Quality Assessment
- Missing values
- Duplicate values
- Data consistency
- Target distribution

# Phase 3: Exploratory Data Analysis (EDA)
- Univariate Analysis
- Bivariate Analysis
- Feature-wise observations
- Business interpretation

# Phase 4: Correlation Analysis
- Correlation Heatmap
- Multicollinearity Check
- Correlation with Target (`price_range`)
- Key Findings

# Phase 5: Data Preprocessing
- Feature & Target Separation
- Train-Test Split
- Feature Scaling (if required)

# Phase 6: Baseline Model Development
- Train baseline models
- Cross Validation

# Phase 7: Model Evaluation
- Accuracy
- Confusion Matrix
- Classification Report
- Performance Comparison

# Phase 8: Feature Engineering & Model Optimization
- Create new features
- Remove/modify features (if justified)
- Retrain models
- Compare with baseline

# Phase 9: Final Model Selection & Prediction
- Select best model
- Train on full training data
- Predict on `test.csv`
- Export final predictions 

# 
Pixel Density / Screen Resolution (px_height × px_width)
Screen Area (sc_h × sc_w)
Camera Score (pc + fc)
Battery Efficiency (battery_power ÷ mobile_wt)
RAM per Core (ram ÷ n_cores)
Storage per Core (int_memory ÷ n_cores)