---
editor: 
  markdown: 
    wrap: 72
---

# Disease Testing Exercise - Student Worksheet

**Name:** Henry Sywulak-Herr **Date:** 11-10-2025

## Your Patient Information

**Patient ID:** 024

**Truth (Red dot?):** \[ \] YES (has disease) \[x\] NO (no disease)

**Model Prediction (Probability):** 0.10

**Deadly Variant? (Star):** \[ \] YES \[x\] NO

------------------------------------------------------------------------

## Round 1: Threshold = 0.50

### Step 1: Your Classification

**Decision rule:** If probability ≥ 0.50 → QUARANTINE

**Where should you go?** \[ \] Quarantine Table\
\[x\] Stay at regular table

### Step 2: What Type of Case Are You?

Based on where you went and your truth:

\[ \] **True Positive (TP)** - Correctly quarantined (have disease, high
prob)\
\[ \] **False Positive (FP)** - Incorrectly quarantined (no disease,
high prob)\
\[x\] **True Negative (TN)** - Correctly not quarantined (no disease,
low prob)\
\[ \] **False Negative (FN)** - Incorrectly not quarantined (have
disease, low prob)

### Step 3: Class-wide Results

Work with your table to count:

```         
           Predicted Positive   Predicted Negative
           (Quarantined)       (Not Quarantined)

Actually 
Positive   TP = 12         FN = 7
(Red Dot)

Actually
Negative   FP = 5         TN = 13
(No Dot)
```

### Step 4: Calculate Metrics

**Sensitivity (True Positive Rate):**
$$\text{Sensitivity} = \frac{TP}{TP + FN} = \frac{12}{12 + 7} = 0.632$$

*Interpretation:* What % of actually sick people did we catch → 63.2%

**Specificity (True Negative Rate):**
$$\text{Specificity} = \frac{TN}{TN + FP} = \frac{13}{13 + 5} = 0.722$$

*Interpretation:* What % of healthy people did we correctly not
quarantine → 72.2%

**Precision (Positive Predictive Value):**
$$\text{Precision} = \frac{TP}{TP + FP} = \frac{12}{12 + 5} = 0.706$$

*Interpretation:* Of those quarantined, what % actually had disease →
70.6%

**Accuracy:**
$$\text{Accuracy} = \frac{TP + TN}{\text{Total}} = \frac{12 + 13}{37} = 0.676$$

*Interpretation:* What % did we classify correctly overall → 67.6%

------------------------------------------------------------------------

## Round 2: Threshold = 0.30

### Your Classification

**Decision rule:** If probability ≥ 0.30 → QUARANTINE

**Where should you go?** \[ \] Quarantine Table \[x\] Stay at regular
table

**Did your classification change from Round 1?** \[ \] YES \[ \] NO

### Class-wide Results

```         
           Predicted Positive   Predicted Negative

Actually 
Positive   TP = 19         FN = 1

Actually
Negative   FP = 10         TN = 7
```

### Calculate Metrics

**Sensitivity:** 0.95 (Did this go up ↑ or down ↓ from Round 1?) *went
way up*

**Specificity:** 0.41 (Did this go up ↑ or down ↓ from Round 1?) *went
way down*

**Precision:** 0.66 *went* *slightly down*

**Accuracy:** 0.70 *went* *slightly up*

### Deadly Variant Check

**How many people with stars (deadly variant) were caught?** - Round 1
(threshold 0.50): \_\_\_\_\_\_\_ - Round 2 (threshold 0.30):
\_\_\_\_\_\_\_

**Did lowering the threshold help catch deadly variants?** ⃝ YES ⃝ NO

------------------------------------------------------------------------

## Round 3: Threshold = 0.70

### Your Classification

**Decision rule:** If probability ≥ 0.70 → QUARANTINE

**Where should you go?** ⃝ Quarantine Table\
⃝ Stay at regular table

### Class-wide Results

```         
           Predicted Positive   Predicted Negative

Actually 
Positive   TP = _______         FN = _______

Actually
Negative   FP = _______         TN = _______
```

### Calculate Metrics

**Sensitivity:** \_\_\_\_\_\_\_

**Specificity:** \_\_\_\_\_\_\_

**Precision:** \_\_\_\_\_\_\_

**Accuracy:** \_\_\_\_\_\_\_

------------------------------------------------------------------------

## Comparison Across Thresholds

Fill in the table below with your results:

| Metric               | Threshold = 0.30 | Threshold = 0.50 | Threshold = 0.70 |
|-------------------|------------------|------------------|------------------|
| Sensitivity          |                  |                  |                  |
| Specificity          |                  |                  |                  |
| Precision            |                  |                  |                  |
| False Positives (FP) |                  |                  |                  |
| False Negatives (FN) |                  |                  |                  |

### Observation Questions

1.  **As threshold increases (0.30 → 0.50 → 0.70), what happens to
    sensitivity?**

    ⃝ Increases ⃝ Decreases ⃝ Stays the same

2.  **As threshold increases, what happens to specificity?**

    ⃝ Increases ⃝ Decreases ⃝ Stays the same

3.  **Can we maximize BOTH sensitivity and specificity at the same
    time?**

    ⃝ YES ⃝ NO

4.  **What is the fundamental trade-off?**

    ------------------------------------------------------------------------

    ------------------------------------------------------------------------

------------------------------------------------------------------------

## Reflection Questions

### Question 1: Personal Experience

**If you were a False Positive (quarantined when healthy):**

How did it feel to be quarantined unnecessarily?

------------------------------------------------------------------------

------------------------------------------------------------------------

What if this meant missing work for 2 weeks without pay? Or being unable
to attend an important event?

------------------------------------------------------------------------

------------------------------------------------------------------------

**If you were a False Negative (missed when actually sick):**

How did it feel to be sent back when you actually had the disease?

------------------------------------------------------------------------

------------------------------------------------------------------------

What if you had the deadly variant (star)? What are the consequences of
being missed?

------------------------------------------------------------------------

------------------------------------------------------------------------

### Question 2: Threshold Choice

**Scenario A: Rare, extremely deadly disease (like Ebola)** - Disease is
rare but 70% fatality rate - Treatment is available and effective if
caught early - Quarantine costs \$1,000/person, treatment costs \$5,000

**Which threshold would you choose?** ⃝ 0.30 ⃝ 0.50 ⃝ 0.70

**Why?**

------------------------------------------------------------------------

------------------------------------------------------------------------

------------------------------------------------------------------------

**Scenario B: Common, mild illness (like common cold)** - Disease is
common but not serious (just annoying) - No treatment available -
Quarantine means missing work (costs \$2,000 in lost wages)

**Which threshold would you choose?** ⃝ 0.30 ⃝ 0.50 ⃝ 0.70

**Why?**

------------------------------------------------------------------------

------------------------------------------------------------------------

------------------------------------------------------------------------

### Question 3: Metrics

**Which metric is MOST important for Scenario A (deadly disease)?**

⃝ Sensitivity - Don't miss any sick people\
⃝ Specificity - Don't quarantine healthy people\
⃝ Accuracy - Overall correct\
⃝ Precision - When we say "sick," be sure

**Why?**

------------------------------------------------------------------------

------------------------------------------------------------------------

**Which metric is MOST important for Scenario B (mild illness)?**

⃝ Sensitivity\
⃝ Specificity\
⃝ Accuracy\
⃝ Precision

**Why?**

------------------------------------------------------------------------

------------------------------------------------------------------------

### Question 4: Real-World Connections

**Think about COVID-19 testing. Rapid tests had lower sensitivity than
PCR tests.**

When might you prefer a rapid test (lower sensitivity)?

------------------------------------------------------------------------

------------------------------------------------------------------------

When would you insist on PCR test (higher sensitivity)?

------------------------------------------------------------------------

------------------------------------------------------------------------

### Question 5: Equity Considerations

**What if the model's predictions were systematically wrong for certain
groups?**

For example: The model gives lower probabilities for women even when
they have the disease.

What would happen?

------------------------------------------------------------------------

------------------------------------------------------------------------

How could we detect this problem?

------------------------------------------------------------------------

------------------------------------------------------------------------

What should we do about it?

------------------------------------------------------------------------

------------------------------------------------------------------------

------------------------------------------------------------------------

## Key Takeaways

**Write 3 key things you learned from this exercise:**

1.  

    ------------------------------------------------------------------------

    ------------------------------------------------------------------------

2.  

    ------------------------------------------------------------------------

    ------------------------------------------------------------------------

3.  

    ------------------------------------------------------------------------

    ------------------------------------------------------------------------

**One question you still have:**

------------------------------------------------------------------------

------------------------------------------------------------------------

------------------------------------------------------------------------
