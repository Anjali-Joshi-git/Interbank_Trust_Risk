# 🏦 Network-Based Systemic Risk Identification  
### A Fragility–Interconnectedness Framework Using Aggregated Interbank Exposure Data

---

## 1. Problem Statement

Modern financial crises have demonstrated that systemic risk does not arise solely from bank size, but from the interaction between:

- Balance sheet fragility  
- Interbank interconnectedness  

Traditional contagion models rely on bilateral exposure matrices, which are rarely publicly available. This creates a practical challenge:

> How can we identify systemically important banks using only aggregated financial statement data?

This project addresses that gap.

---

## 2. Research Question

> Which banks pose the greatest systemic risk when considering both financial fragility and interbank interconnectedness?

---

## 3. Proposed Solution

We construct a two-dimensional systemic risk framework combining:

1. **Internal Vulnerability (Fragility)**
2. **External Connectivity (Interbank Embeddedness)**

A bank is considered systemically important only when it ranks high on both dimensions simultaneously.

---

## 4. Methodology

### 4.1 Financial Fragility Index

We constructed a composite `systemic_risk_index` using standardized versions of:

- Leverage Ratio  
- Equity Ratio  
- Interbank Funding Ratio  
- Log(Total Assets)

This index captures structural balance sheet weakness and funding vulnerability.

---

### 4.2 Exposure-Based Network Proxy

Since bilateral interbank exposure data was unavailable, we approximated network embeddedness using:


This measures how dependent a bank is on the interbank system relative to its size.

---

### 4.3 Joint Systemic Ranking

Banks were ranked based on their joint position in:

- Fragility space  
- Interconnectedness space  

Institutions in the top quantiles of both metrics were classified as systemically important.

---

## 5. Empirical Findings

### 📌 Correlation Analysis

Correlation between fragility and interconnectedness:


Interpretation:
- Financial fragility and interbank embeddedness are weakly related.
- Large or fragile banks are not automatically highly interconnected.

---

### 📌 Distribution of Interbank Strength

- Mean: 0.033  
- Median: 0.017  
- 75th percentile: 0.039  
- Maximum: 0.427  

Most banks maintain low interbank exposure (<4% of total assets), while a small subset exhibits significantly higher dependency.

---

### 📌 Structural Insight

Systemic risk is:

- Highly skewed  
- Concentrated among a limited subset of institutions  
- Not purely size-driven  

True systemic importance emerges only when fragility and interconnectedness coexist.

---

## 6. Answer to the Research Question

The banks that pose the greatest systemic risk are those that:

- Exhibit high leverage and funding vulnerability  
- Maintain substantial interbank exposure relative to assets  
- Rank in the upper-right quadrant of the fragility–interconnectedness space  

These institutions have the highest potential to:

- Amplify shocks internally due to weak balance sheets  
- Transmit distress externally through funding network linkages  

---

## 7. Key Contribution

This project demonstrates that systemic importance can be estimated using aggregated exposure data by combining:

- Balance sheet fragility  
- Interbank embeddedness  

The framework is:

- Interpretable  
- Scalable  
- Computationally efficient  
- Implementable using regulatory datasets  

---

## 8. Limitations

- No bilateral exposure matrix → no true contagion cascade simulation  
- Network centrality metrics collapse under aggregated structure  
- Results measure vulnerability, not realized default propagation  

---

## 9. Conclusion

Systemic importance is not driven solely by size.

It emerges from the interaction between:

- Internal financial weakness  
- External network connectivity  

Banks that are simultaneously fragile and deeply embedded within the interbank system pose the greatest systemic threat.

This framework provides a practical and defensible approach to systemic risk monitoring when detailed exposure data is unavailable.

---

## 10. Future Work

- Incorporate bilateral exposure matrices  
- Implement default cascade simulation  
- Extend to time-series systemic risk tracking  
- Compare against market-based systemic risk measures  

---

**Author:** Anjali Joshi  
Financial Risk Analytics | Network Modeling | Systemic Risk Research
