# XGEM
1. The program is edited with jupyter notebook, using python language, and the suffix is ​​.ipynb.

2. + Five weak classifier results: in the "weak classifier" folder.
   + The extraction method name ".ipynb is named after DecisionTree and models built by different extraction methods.
   + For example: DecisionTree+Kmer4.ipynb represents the model constructed by decision tree and Kmer.

3. + Five strong classifier results, in the "strong classifier" folder.
   + The naming methods are all models built by XgBoost and different feature extraction methods. Such as: XgBoost+Mismatch21.ipynb said
Classification model built by XgBoost and Mismatch.

4. Comparative test: in the "comparison" folder. XGBoost+Mismatch. ipynb means 77 positive samples and 77 negative samples Show results on my method.

5. All the data used in the experiment are summarized in the "dataset" folder, where the dataset folder contains three folders: 
   + dataset1 Contains 77 positive samples and 77 negative samples and their characteristics used for comparative experiments; 
   + dataset2 contains 85 positive samples and 88 used for comparative experiments Negative samples and their features; 
   + dataset3 contains the remaining pre-miRNA sequences and features after removing the experimental data.
