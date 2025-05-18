# SCT_ML_02
SCT-ML-2: Customer Segmentation using K-means Clustering

![Customer Clusters Visualization](output/clusters.png)

📋 Table of Contents
- [Task Overview](#-task-overview)
- [Repository Structure](#-repository-structure)
- [Setup Instructions](#-setup-instructions)
- [Execution Guide](#-execution-guide)
- [Results](#-results)
- [Key Findings](#-key-findings)
- [Technical Specifications](#-technical-specifications)
- [License](#-license)

🎯 Task Overview
Objective: Implement K-means clustering to segment mall customers based on their purchasing behavior.

Input Features:
1. Annual Income (k$)
2. Spending Score (1-100)

Expected Output:
- Optimal number of customer segments
- Visualization of clusters
- Business recommendations for each segment

#🗂 Repository Structure

SCT-ML-2/
├── data/
│   └── Mall_Customers.csv          # Dataset
├── notebooks/
│   ├── EDA.ipynb                   # Exploratory analysis
│   └── Clustering_Analysis.ipynb   # Main task notebook
├── src/
│   ├── kmeans.py                   # Core clustering logic
│   └── utils.py                    # Helper functions
├── output/
│   ├── clusters.png                # Final cluster visualization
│   ├── elbow_plot.png              # WCSS analysis
│   └── silhouette_plot.png         # Cluster quality
├── requirements.txt                # Dependencies
├── LICENSE                         # MIT License
└── README.md                       # This file

#⚙️ Setup Instructions

# Prerequisites
- Python 3.8+
- pip package manager

# Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/SCT-ML-2.git
   cd SCT-ML-2
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## 🚀 Execution Guide

# Option 1: Jupyter Notebook
```bash
jupyter notebook notebooks/Clustering_Analysis.ipynb
```

# Option 2: Python Script
```bash
python src/kmeans.py
```

# Expected Output
The script will:
1. Generate cluster visualizations in `/output`
2. Print cluster statistics to console
3. Save model artifacts (if implemented)

# 📊 Results

# Cluster Characteristics
| Cluster | Avg. Income | Avg. Spending | Size | Interpretation |
|---------|------------|--------------|------|----------------|
| 0       | 88k        | 17           | 23%  | High-income cautious spenders |
| 1       | 55k        | 49           | 35%  | Balanced customers |
| 2       | 86k        | 82           | 15%  | Premium targets |
| 3       | 26k        | 78           | 19%  | Value seekers |
| 4       | 25k        | 22           | 8%   | Low engagement |

# Visualizations
1. **Elbow Method Plot** (`output/elbow_plot.png`)
2. **Silhouette Analysis** (`output/silhouette_plot.png`)
3. **Final Clusters** (`output/clusters.png`)

# 🔍 Key Findings
1. Optimal Clusters: 5 (validated by elbow method and silhouette score)
2. Most Valuable Segment: Cluster 2 (High income + High spending)
3. Growth Opportunity: Cluster 3 responds well to discounts
4. Underperforming: Cluster 4 needs reactivation campaigns

# 💻 Technical Specifications

# Algorithms Used
- K-means Clustering
- Elbow Method (WCSS)
- Silhouette Analysis

# Dependencies
```text
numpy==1.21.2
pandas==1.3.4
scikit-learn==0.24.2
matplotlib==3.4.3
seaborn==0.11.2
jupyter==1.0.0
```

# Hyperparameters
```python
KMeans(
    n_clusters=5,
    init='k-means++',
    max_iter=300,
    random_state=42
)
```

# 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
Created for SCT Machine Learning Internship Task 2
```

### Key Features:
1. **Complete Structure**: All essential sections for an ML project
2. **Track-Specific**: Follows `SCT-ML-<TaskNumber>` convention
3. **Visual Elements**: Ready for images/outputs
4. **Technical Depth**: Includes hyperparameters and algorithms
5. **Business Focus**: Clear interpretations for each cluster

### How to Use:
1. Replace placeholders (`your-username`, file paths)
2. Add your actual output images to `/output`
3. Update cluster interpretations based on your analysis
4. Customize the technical specs as needed
