# medication-association-rules-analysis
Market basket analysis to identify significant associations between medication classifications using the Apriori algorithm and lift analysis.

## Project Overview
This project applies market basket analysis techniques to identify significant associations between medication classifications prescribed to patients. Using the Apriori algorithm and lift analysis, this study uncovers meaningful prescription patterns that could guide healthcare providers in optimizing medication combinations and potentially reducing hospital readmission rates.

## Key Findings
- **Top Three Association Rules**:
  1. Antibiotics → Antihypertensives (Lift: 2.54, Confidence: 0.60)
  2. Anti-Inflammatories → Antihypertensives (Lift: 2.66, Confidence: 0.63)
  3. Antipsychotics → Antihypertensives (Lift: 2.61, Confidence: 0.62)

- **Strong Predictive Relationships**: Patients prescribed antibiotics, anti-inflammatories, or antipsychotics were approximately 2.5 times more likely to also receive antihypertensives than by random chance

- **Frequent Combinations**: These medication associations appeared in 6-7.5% of all patient prescriptions, indicating common prescription patterns

- **Medical Rationale**: The associations align with medical understanding of how these conditions interact (e.g., hypertension's connection to inflammation and immune function)

## Business Value
Healthcare providers can leverage these insights to:
- Identify potentially more effective medication combinations
- Evaluate how different prescription patterns correlate with readmission rates
- Develop more targeted treatment protocols for patients with multiple conditions
- Reduce financial penalties from the Centers for Medicare and Medicaid Services (CMS) by optimizing prescription practices
- Improve overall patient care through data-driven medication management

## Technologies Used
- Python (Pandas, NumPy)
- MLxtend library for Apriori algorithm implementation
- Matplotlib & Seaborn for visualization
- Association rule metrics (support, confidence, lift)

## Methodology
1. **Data Preprocessing**: 
   - Aggregated 119 individual medications into 30 broader classifications
   - Transformed prescription data into a transaction format suitable for association rule mining
   - Converted medication presence/absence to boolean values

2. **Association Rule Mining**:
   - Applied Apriori algorithm to identify frequent item sets with minimum support of 0.001
   - Generated association rules from frequent item sets
   - Calculated support, confidence, and lift metrics for each rule

3. **Rule Evaluation and Selection**:
   - Filtered rules using thresholds (support > 0.06, lift > 2.5, confidence > 0.5)
   - Identified top three rules based on these metrics
   - Analyzed the medical significance of these associations

## Key Visualizations
- Association rules matrix displaying the relationships between medication classifications
- Heatmap of the principal component loadings
- Metric charts showing support, confidence, and lift values for top rules

## Future Work
- Analyze how these medication associations correlate with readmission rates
- Explore demographic variations in prescription patterns
- Investigate specific medications within these classifications for more granular insights
- Develop predictive models to guide prescription decisions based on patient characteristics

---

*Note: This analysis was conducted for educational purposes and should not influence clinical decisions without proper medical evaluation.*
