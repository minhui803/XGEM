# XGEM

In this work, we predict essential miRNA by the ensembles of various sequence-based classifiers with XGBoost algorithm. All the data used in the experiment are summarized in the **"dataset"** folder, including,  **dataset1**(It contains 77 positive samples and 77 negative samples for comparative experiments), **dataset2**(It contains 85 positive samples and 88 negative samples for train model), **dataset3**(All mouse pre-miRNA sequences after removing the experimental data), **dataset4**(It contains 8 essential miRNAs and 8 non-essential miRNAs that we collected). **dataset5**(It contains feature data for feature extraction methods under different combinations of parameters).

# How to run

The program was edited and run using jupyter notebook, using python 3.8. The suffixes are all .ipynb.

Configuration Environment

Install jupyter notebook, you should type in the terminal：

`pip install jupyter`

Install required packages, you should type in the terminal:

`pip install numpy matplotlib scikit-learn pandas -i https://pypi.tuna.tsinghua.edu.cn/simple`

Start jupyter notebook, you should type in the terminal:

`jupyter notebook`

Then, run  the  .ipynb file in the corresponding folder.The specific records are as follows:

   | Folder Name        | Detailed Content                                             |
   | ------------------ | ------------------------------------------------------------ |
   | weak classifier    | It contains five base classifiers, CART+kmer.ipynb, CART+Mismatch.ipynb, CART+PseDSSPC.ipynb, CART+Subsequence.ipynb and CART+Triplet.ipynb. |
   | strong classifier  | It contains five strong classifiers, XGBoost+kmer.ipynb, XGBoost+Mismatch.ipynb, XGBoost+PseDSSPC.ipynb, XGBoost+Subsequence.ipynb and XGBoost+Triplet.ipynb. |
   | indep_dataset_test | It contains the prediction process using an independent test set. Mismatch.ipynb represents using the XGBoost+Mismatch model for prediction. Subsequence.ipynb represents using the XGBoost+Subsequence model for prediction. |
   | comparison         | It contains comparative experimental procedures. XGEM.ipynb represents that XGEM uses a five-fold cross-validation process. |
   | prediction         | It contains all mouse pre-miRNA sequences after removing experimental data using XGEM prediction. The detailed code is recorded in XGEM.ipynb    | adjust_parameter   | It contains the parameter adjustment proces of k-mer, mismatch,subsequence,PseDSSPC.|
   

# How to predict other types of genomes

- First, you need to have the sequence information of the gene. Extract the sequence feature information by BioSeq-Analysis 2.0(http://bioinformatics.hitsz.edu.cn/BioSeq-Analysis/RNA). Choose the mismatch feature extraction method, the parameter *k* is 2 and *m* is 1. 
- Then, name the extracted feature information Mismatch, store it in the **pred_other_essen_gene** folder in .csv format.
- Finally, execute the XGEM.ipynb file in the corresponding folder. The output will have two forms: 0 or 1. 0 represents that the predicted gene is non-essential. 1 represents that the predicted gene is essential.



 





