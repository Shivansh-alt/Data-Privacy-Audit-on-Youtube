# Data Anonymization Techniques

**Data anonymization** is the process of modifying personal or sensitive data so that individuals cannot be easily identified from the dataset.

Three common techniques are **k-anonymity, differential privacy, and data masking**.

## 1. K-Anonymity

**K-anonymity** ensures that each person's record is indistinguishable from at least **k − 1 other records** with respect to selected identifying attributes.

For example:

| Name | Age | City | Disease |
|---|---:|---|---|
| Rahul | 23 | Delhi | Flu |
| Amit | 24 | Delhi | Cold |
| Priya | 25 | Delhi | Flu |
| Neha | 23 | Mumbai | Cold |

Remove the names and generalize the age:

| Age Group | City | Disease |
|---|---|---|
| 20–29 | Delhi | Flu |
| 20–29 | Delhi | Cold |
| 20–29 | Delhi | Flu |
| 20–29 | Mumbai | Cold |

If **Age Group + City** identifies at least 2 records in every group, the dataset satisfies **2-anonymity**.

**Used for:** Releasing datasets while reducing the risk of re-identification.

---

## 2. Differential Privacy

**Differential privacy (DP)** protects individuals by adding carefully controlled **random noise** to query results.

Suppose a hospital dataset contains:

```text
Total patients = 10,000
Diabetes patients = 2,500
```

Instead of publishing the exact number:

```text
Diabetes patients = 2,500
```

a differentially private system might publish:

```text
Diabetes patients ≈ 2,493
```

The noise makes it difficult to determine whether any particular person's data contributed to the result.

A common mechanism is **Laplace noise**:

```text
Private result = Actual result + Random noise
```

**Used for:** Statistical databases, research systems, and large-scale data analysis.

---

## 3. Data Masking

**Data masking** replaces sensitive values with altered or hidden values while retaining enough structure for testing or analysis.

Original:

| Name | Phone | Email |
|---|---|---|
| Rahul Sharma | 9876543210 | rahul@example.com |

Masked:

| Name | Phone | Email |
|---|---|---|
| R**** S***** | XXXXXXX210 | r****@example.com |

Common masking methods include:

- **Character masking:** `9876543210 → XXXXXXX210`
- **Partial masking:** `rahul@example.com → r****@example.com`
- **Substitution:** Replace real names with synthetic names
- **Tokenization:** Replace sensitive values with tokens

**Used for:** Software testing, databases, and internal data sharing.

---

# Applying Anonymization to a Real-World Dataset

Consider a **hospital patient dataset**:

| Name | Age | ZIP Code | Disease | Phone |
|---|---:|---|---|---|
| Rahul | 23 | 110001 | Flu | 9876543210 |
| Amit | 24 | 110001 | Cold | 9876543211 |
| Priya | 25 | 110001 | Flu | 9876543212 |
| Neha | 23 | 400001 | Cold | 9876543213 |

## Step 1 — Data Masking

Remove or mask direct identifiers:

```text
Name → Removed
Phone → XXXXXXX210
```

The goal is to prevent direct identification of patients.

## Step 2 — K-Anonymity

Generalize quasi-identifiers:

```text
Age: 23, 24, 25 → 20–29
ZIP: 110001 → 110***
```

Result:

| Age Group | ZIP | Disease |
|---|---|---|
| 20–29 | 110*** | Flu |
| 20–29 | 110*** | Cold |
| 20–29 | 110*** | Flu |
| 20–29 | 400*** | Cold |

The records are now less directly identifiable.

> **Note:** This simplified example illustrates the technique. A real k-anonymity assessment must check every combination of selected quasi-identifiers and verify that the required k value is satisfied.

## Step 3 — Differential Privacy

For statistical analysis, instead of publishing the exact number of patients with a disease:

```text
Actual: Flu patients = 2
```

publish a noisy result such as:

```text
Differentially private result ≈ 3
```

The exact noise and privacy parameters would be selected according to the privacy requirements.

---

# Comparison

| Technique | Main Protection | Basic Approach |
|---|---|---|
| **K-anonymity** | Re-identification through combinations of attributes | Generalization and suppression |
| **Differential privacy** | Inferring whether an individual's data affected a result | Add mathematically controlled noise |
| **Data masking** | Exposure of sensitive fields | Hide or replace values |

## Key Takeaway

```text
Data Masking          → Hide sensitive values
K-Anonymity           → Make individuals less distinguishable
Differential Privacy → Add controlled noise to analysis
```

In a real-world privacy system, these techniques can also be **combined** rather than relying on only one method.
