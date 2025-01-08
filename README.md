# Credit Default Risk Analysis

## Overview

This analysis explores patterns in bank loan data to identify factors indicating clients' difficulty in repaying loans. The study utilizes three datasets:
- **Application Data**: Information of current applicants.
- **Previous Application Data**: Applicants' loan history.
- **Column Descriptions**: Metadata detailing the attributes of the datasets.

## Data Preparation

### Cleaning Process
- **Application Dataset**:
  - Started with 307,511 rows and 122 columns.
  - Removed 77 columns due to high missing values or lack of relevance.
- **Previous Application Dataset**:
  - Started with 1,670,214 rows and 37 columns.
  - Removed 13 columns due to similar issues.

### Data Treatment
1. **Missing Value Treatment**:
   - Median imputation for variables with significant outliers.
   - Mean imputation for variables with normal distribution.
   - Mode imputation for categorical variables.
   
2. **Outlier Handling**:
   - Preserved outliers in critical variables (e.g., age, income, children).
   - Applied binning strategy for outliers instead of removal.
   
3. **Standardization**:
   - Converted negative values to absolute (e.g., DAYS_BIRTH).

## Key Findings

### Demographic Patterns
1. **Age**:
   - Highest risk: 20-30 years.
   - Risk decreases with age.
   - Most stable borrowers: 40-50 years (25% of applications).
   
2. **Gender**:
   - Males: Higher default rate (~10%).
   - Females: Lower default rate (~7%).
   - Female applicants comprise about 65% of total applications.

3. **Family**:
   - Lowest risk: Applicants with no children (70% of applications).
   - Highest risk: Applicants with 9-11 children.
   - Most loans taken by people with 2 family members.

### Financial Indicators
1. **Income**:
   - Most common: 100-150k annual salary (~30% of applications).
   - Higher risk: 100-150k income group (~8.5% default rate).
   - Lower risk: 200-250k income group.

2. **Loan Characteristics**:
   - Most common loan amount: 200k-300k.
   - Most popular loan type: Cash loans (90% of applications).
   - Cash loans have the highest default rate (~8.5%).

### Educational and Housing Factors
1. **Education**:
   - Lowest risk: Higher education graduates.
   - Higher risk: Secondary education graduates.
   - Highest risk: Lower secondary education combined with certain housing types.

2. **Housing**:
   - Lowest risk: House/apartment owners.
   - Highest risk:
     - Rented apartment residents.
     - Those living with parents.
   - Most applications: House/apartment owners.

### Employment Factors
1. **Occupation**:
   - Most applications: Laborers (9% default rate).
   - Highest risk: Low-skilled laborers.
   - Employment duration shows negative correlation with default rate.

2. **Income Type**:
   - Lowest risk: "Working" category.
   - Moderate risk: Commercial associates (~8% default rate).
   - Highest risk: Maternity leave and unemployed categories.

### Previous Loan Behavior
1. **Application Status**:
   - 62% approved.
   - 20% cancelled.
   - 18% refused.
   - 0.3% unused.

2. **Customer Type**:
   - 72% repeat borrowers.
   - 18% new applications.
   - Previously refused applications show 12% default rate in current loans.

## Recommendations

### Preferred Applicant Profile:
- **Age**: 40-50 years.
- **Education**: Higher education.
- **Housing**: House/apartment owners.
- **Employment**: Stable employment with significant experience.
- **Income**: 200k-250k range.
- **Family**: 0-2 children.

### High-Risk Indicators:
- **Young applicants** (20-30 years).
- **Low-skilled laborers**.
- **Rented accommodation** or living with parents.
- Multiple credit bureau requests.
- Previous loan refusals.
- Unemployed or on maternity leave.
- Lower secondary education.

### Additional Considerations:
- Scrutinize **cash loan** applications more carefully.
- Consider the applicant's **social circle** for potential default risks.
- Pay special attention to **high-value loans** (400k-500k range).
- Evaluate **previous loan history** thoroughly.
- Consider the **stability of employment** and income source.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

