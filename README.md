# A/B Test Ecommerce Checkout Optimization

## Overview
This project evaluates whether a redesigned e‑commerce checkout flow improves conversion rates compared to the existing experience. Using a dataset of 10,000 simulated shoppers, I ran a full A/B test, validated the integrity of the experiment, 
and quantified the business impact of the new design.

The analysis includes:
- Conversion rate comparison  
- Two‑sample proportion z‑test  
- Confidence intervals  
- Minimum Detectable Effect (MDE) power analysis  
- Sample Ratio Mismatch (SRM) validation using a Chi‑Square goodness‑of‑fit test 


## Goal    
The goal was to determine whether a redesigned e‑commerce checkout page leads to a statistically significant improvement in conversion and whether the experiment was properly randomized and sufficiently powered to detect a meaningful 
lift.


## Resources Used
- Coding Environment: Google Colab (extension for Visual Studio Code)
- AI Copilot: ChatGPT (debug and interpret results)
- Python 3.7 libraries: 
    - Pandas (data handling)
    - Matplotlib for data visualization
    - statsmodels (statistical math) and scipy.stats (probability distributions)


## Dataset
The dataset includes 10,000 shoppers randomly assigned to:
- **Control** (existing checkout)
- **Treatment** (redesigned checkout)


## Key Analyses

### **1. Conversion Rates**
The conversion rates comparison illustrates a **2%** lift.
- **12.35% for the control group**
- **14.56% for the treatment group**


image - KDEs for Calculated Conversion Distributions


### **2. Two‑Sample Z‑Test**
A two‑sample proportion z‑test was used to determine whether the difference in conversion rates was statistically significant.

### **3. Confidence Intervals**
95% confidence intervals were calculated for both variants to quantify uncertainty around the conversion estimates.

### **4. Minimum Detectable Effect (MDE) Power Analysis**
Using `statsmodels.stats.power`, I evaluated whether the sample size was large enough to reliably detect a
**2‑percentage‑point lift** — a meaningful business improvement.

The experiment achieved **high statistical power**, confirming that the sample size was sufficient.

### **5. Sample Ratio Mismatch (SRM) Check**
To ensure the assignment mechanism was not biased or broken, I performed an SRM check using a 
**Chi‑Square goodness‑of‑fit test** on **unique users per group**.  
This validated that the observed group split matched the expected 50/50 allocation.


## **Results Summary**
- The redesigned checkout page produced a **statistically significant lift** in conversion.  
- The p‑value was well below 0.05, indicating the improvement is unlikely due to chance.  
- Power analysis confirmed the experiment was sufficiently sized to detect the target lift.  
- SRM validation showed no assignment issues — the experiment was trustworthy.  

**Recommendation:** Roll out the redesigned checkout experience to 100% of traffic.

