Assignment-1: Probability Density Function (PDF) Learning

Roll Number: 102303778

------------------------------------------------------------

OBJECTIVE

The objective of this assignment is to learn the Probability Density Function (PDF) of a transformed random variable derived from real-world NO₂ (Nitrogen Dioxide) concentration data. The transformation and PDF parameters are uniquely determined using the student’s roll number.

------------------------------------------------------------

DATASET DESCRIPTION

File Name: data.csv
Column Used: no2
Description: Contains NO₂ (Nitrogen Dioxide) concentration values

Preprocessing Steps:
- Removed missing values
- Converted data to floating-point format

------------------------------------------------------------

METHODOLOGY

Step 1: Load Dataset

The dataset is loaded using the Pandas library. Only valid NO₂ values are retained for further analysis.

x = df["no2"].dropna().astype(float)

------------------------------------------------------------

Step 2: Roll Number Based Parameters

To ensure uniqueness of the model, transformation parameters are derived from the roll number.

Roll Number = 102303778

a_r = 0.05 × (roll % 7)
b_r = 0.3 × (roll % 5 + 1)

Computed Values:
a_r = 0.15
b_r = 1.2

------------------------------------------------------------

Step 3: Variable Transformation

The original variable x is transformed into a new variable z using the equation:

z = x + a_r × sin(b_r × x)

This transformation introduces controlled non-linearity in the data.

------------------------------------------------------------

Step 4: Learning the Probability Density Function

The transformed variable z is modeled using a Gaussian-like probability density function:

p(z) = c × exp(-λ (z − μ)²)

Where:
μ = Mean of transformed variable z
Variance = Variance of z
λ = 1 / (2 × Variance)
c = √(λ / π)

------------------------------------------------------------

RESULTS

Learned PDF Parameters:

μ : Mean of transformed variable
λ : Spread parameter of PDF
c : Normalization constant

(Exact numerical values depend on the dataset)

------------------------------------------------------------

RESULT GRAPH

- Histogram of the transformed variable z
- Fitted PDF curve plotted over the histogram
- The fitted curve closely matches the histogram, validating the learned PDF

Graph Title:
Histogram of Transformed Variable z with Fitted PDF

------------------------------------------------------------

OBSERVATIONS

- Roll-number-based parameters ensure unique results
- The transformed data follows a smooth distribution
- Gaussian PDF provides a good approximation
- Sampling improves plotting efficiency without loss of accuracy

------------------------------------------------------------

TOOLS AND LIBRARIES USED

- Python
- NumPy
- Pandas
- Matplotlib

------------------------------------------------------------

CONCLUSION

This assignment successfully demonstrates data preprocessing, non-linear transformation, PDF parameter estimation, and visualization. The learned probability density function accurately models the transformed NO₂ concentration data.

------------------------------------------------------------
