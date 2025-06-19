**AI-Driven Unsupervised Clustering of Maternal Health Risk Profiles**
**Contributing to SDG 3: Good Health and Well-being
**

**Introduction**

One of the core goals of Sustainable Development Goal 3 (SDG 3) is to ensure healthy lives and promote well-being for all, at all ages. A critical target under this goal is to reduce the global maternal mortality ratio to less than 70 per 100,000 live births by 2030. While maternal health systems have improved in many parts of the world, emerging lifestyle and demographic changes, such as older maternal age due to career prioritization, are introducing new, often underestimated risk factors.

This project aims to uncover hidden patterns of maternal risk using machine learning, specifically unsupervised learning. Rather than manually labeling women as “high risk” or “low risk,” we allow an AI model to discover natural groupings within the data. These insights can support early intervention and more equitable maternal health strategies.

**Methodology**
 1. Dataset
We used a dataset containing over 8,800 maternal health records, featuring more than 600 clinical and demographic attributes. Key selected features included:

Maternal age, weight, and height

Number of pregnancies, stillbirths, live births

Pregnancy duration

Antenatal care visits

Birth outcomes (e.g., birth weight)

 2. Data Preprocessing
Missing values were filled with mean values for consistency.

Features were standardized using StandardScaler to give each variable equal weight.

Dimensionality reduction was performed using PCA (Principal Component Analysis) to enable visualization of high-dimensional relationships.

3. Unsupervised Learning with K-Means Clustering
We applied K-Means Clustering (k=3) to group mothers into three natural clusters based solely on health data, without predefined labels. The PCA projection below shows the resulting clusters:

![image](https://github.com/user-attachments/assets/0eb52ce9-6152-4f3d-a582-311509908d4e)

PCA visualization showing the natural separation of maternal profiles in 2D.

![image](https://github.com/user-attachments/assets/8177688d-4f01-4dfc-8227-1e4ac97b4015)

Each point represents a mother; color-coded clusters were generated purely based on shared traits like age, parity, and antenatal care.

 4. Cluster Profiling and Risk Interpretation
After clustering, we analyzed the mean of key features within each cluster:

Feature	Cluster 0<br>🔴 High Risk	Cluster 1<br>🟢 Low Risk	Cluster 2<br>🟡 Moderate Risk
Age	34.85	24.60	25.76
# Pregnancies	6.12	2.21	2.00
Stillbirths	0.22	1.44	2.72
Pregnancy Duration (weeks)	26.05	24.32	17.84
Birth Weight (kg)	4.39	3.31	3.23
Antenatal Visits	2.67	3.13	3.05

Based on this analysis, we defined the following risk profiles:

🔴 Cluster 0 – High Risk: Older women, many pregnancies, high birth weights (risk of macrosomia), low ANC visits.

🟢 Cluster 1 – Low Risk: Young mothers, low parity, good ANC attendance, healthy weights.

🟡 Cluster 2 – Moderate Risk: Younger women with concerning stillbirth history and short pregnancy durations.

 5. Visualizing Risk Profiles
 Radar Chart
To clearly visualize how each group compares across features, we generated a radar plot:
![image](https://github.com/user-attachments/assets/bf832f92-9981-4ce3-be43-da72f86f76df)


Each line shows the average normalized values for each cluster across the 10 features.

High Risk (Blue): Peaks in parity and weight

Low Risk (Orange): Strong antenatal engagement

Moderate Risk (Green): Spikes in stillbirths and poor outcomes

💡 Insights & Impact
This unsupervised model highlights clinically relevant groupings of maternal profiles — helping uncover risk clusters that may not be obvious with manual screening. Importantly:

It provides a data-driven basis for targeting interventions.

It could improve resource allocation in overstretched maternal health systems.

It reveals non-obvious risks — such as younger women with poor outcomes.

⚖️ Ethical Considerations
Bias & Representation: The dataset may underrepresent rural or marginalized communities.

Interpretability: Though AI groups patterns, clinical interpretation is essential.

Complementarity: This model should support, not replace, healthcare worker judgment.

✅ Conclusion
By using unsupervised learning to cluster maternal health data, we demonstrate how machine learning can uncover emerging patterns in maternal risk — supporting more personalized, preventive care. This work directly aligns with SDG 3: Good Health and Well-being, and showcases the power of AI in solving critical public health challenges.

