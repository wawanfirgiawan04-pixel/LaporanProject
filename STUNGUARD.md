# STUNGUARD
## WHO LMS-Based Anthropometric Calculator for Children Aged 0–60 Months

---

# 1. Project Overview

STUNGUARD is an offline anthropometric assessment application designed to evaluate the nutritional and growth status of children aged 0–60 months using the WHO Child Growth Standards and LMS (Lambda-Mu-Sigma) method.

The application focuses on:
- Weight-for-Age (WFA)
- Length/Height-for-Age (LFA/HFA)
- Weight-for-Length (WFL)
- BMI-for-Age (BMIFA)

The application calculates WHO-standard Z-scores and classifies child nutritional status such as:
- Normal
- Underweight
- Stunted
- Severely Stunted
- Overweight
- Obesity

---

# 2. Main Objectives

The objectives of STUNGUARD are:

1. To provide an offline anthropometric calculator.
2. To assist early detection of stunting and malnutrition.
3. To implement WHO LMS methodology.
4. To support Posyandu and healthcare screening systems.
5. To provide WHO-compatible anthropometric calculations.

---

# 3. Technologies Used

| Technology | Function |
|---|---|
| Python | Main Programming Language |
| PySide6 | GUI Framework |
| Pandas | CSV Dataset Processing |
| Math | LMS Calculation |
| WHO LMS Dataset | Anthropometric Standards |

---

# 4. Anthropometric Indicators

## 4.1 Weight-for-Age (WFA)

Measures body weight according to child age.

### Interpretation

| Z-Score | Classification |
|---|---|
| < -3 SD | Severely Underweight |
| -3 SD to < -2 SD | Underweight |
| -2 SD to +1 SD | Normal |
| > +1 SD | Risk of Overweight |

---

## 4.2 Length-for-Age (LFA)

Measures body length/height according to age.

### Interpretation

| Z-Score | Classification |
|---|---|
| < -3 SD | Severely Stunted |
| -3 SD to < -2 SD | Stunted |
| -2 SD to +3 SD | Normal |
| > +3 SD | Tall |

---

## 4.3 Weight-for-Length (WFL)

Measures weight relative to body length/height.

### Interpretation

| Z-Score | Classification |
|---|---|
| < -3 SD | Severe Wasting |
| -3 SD to < -2 SD | Wasting |
| -2 SD to +1 SD | Normal |
| +1 SD to +2 SD | Risk of Overweight |
| +2 SD to +3 SD | Overweight |
| > +3 SD | Obesity |

---

## 4.4 BMI-for-Age (BMIFA)

Measures Body Mass Index according to age.

### Interpretation

| Z-Score | Classification |
|---|---|
| < -3 SD | Severe Wasting |
| -3 SD to < -2 SD | Wasting |
| -2 SD to +1 SD | Normal |
| +1 SD to +2 SD | Risk of Overweight |
| +2 SD to +3 SD | Overweight |
| > +3 SD | Obesity |

---

# 5. WHO LMS Method

The application uses the WHO LMS Method.

LMS consists of:

| Parameter | Description |
|---|---|
| L | Lambda (Box-Cox Power) |
| M | Median |
| S | Coefficient of Variation |

---

# 6. WHO LMS Formula

If:

```math
L ≠ 0