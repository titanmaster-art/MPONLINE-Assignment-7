# Customer Segmentation using K-Means Clustering and PCA

**Author:** ARIGHNA  GUPTA  

**Registration Number:** 23BCY10207 



**Batch Number:** 5A



## Objective
The objective of this project is to segment mall customers into distinct behavioral groups based on demographic details, annual income, and spending scores using K-Means clustering, and visualize the segments in 2D using Principal Component Analysis (PCA).

## Dataset Link
- [Kaggle: Mall Customer Segmentation Dataset](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)

## Libraries Used
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `kaggle`

## Methodology
1. **Data Understanding**: Identified numerical (`Age`, `Annual Income`, `Spending Score`) and categorical (`Gender`) attributes.
2. **Data Preprocessing**:
   - Confirmed zero missing values.
   - Dropped non-informative identifier `CustomerID`.
   - Binary encoded `Gender` (`Male`: 1, `Female`: 0).
   - Standardized features using `StandardScaler`.
3. **Model Development**:
   - Used the Elbow Method (WCSS) to select optimal clusters ($K = 5$).
   - Trained `KMeans` with $K = 5$ to assign cluster labels.
   - Applied `PCA(n_components=2)` for dimensionality reduction.
4. **Visualization**: Plotted the Elbow Curve, Customer Segment distributions, and 2D PCA Cluster projections.

## Results
- **Optimal Clusters ($K$):** 5 distinct customer groups.
- **PCA Variance Explained:** Component 1 (33.69%) + Component 2 (26.23%) = **59.92% Total Variance Explained**.
- **Segments Identified**:
  1. *High Income, High Spending*: Target VIP Customers.
  2. *High Income, Low Spending*: Potential growth segment.
  3. *Low Income, High Spending*: Impulsive shoppers.
  4. *Low Income, Low Spending*: Frugal shoppers.
  5. *Average Income, Moderate Spending*: Mainstream baseline customers.

## Conclusion
Combining K-Means clustering with PCA enables effective multidimensional customer segmentation for targeted marketing campaigns. While K-Means is restricted by spherical cluster assumptions, PCA effectively simplifies high-dimensional feature spaces for clear business insight.
