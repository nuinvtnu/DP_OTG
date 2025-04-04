## **DP_OTG**
**DP_OTG**: a novel deep learning model for human OTG site prediction that integrates 1D Convolutional Neural Networks (CNN1D) and Bidirectional Long Short-Term Memory (Bi-LSTM) networks. Our model employs an NLP-based word embedding technique with trainable embeddings, allowing it to dynamically learn optimized sequence representations directly from raw protein sequences. The CNN1D module, consisting of five convolutional layers operating in parallel with three different kernel sizes, captures local sequence motifs of varying lengths. Meanwhile, the Bi-LSTM layer learns long-range dependencies, enhancing contextual feature extraction. The extracted features from CNN1D and Bi-LSTM are fused to generate a comprehensive feature representation, which is processed through fully connected layers and a final sigmoid activation for binary classification.

## Requirement
   - Keras
   - Numpy
   - Sklearn
   - Pandas
   - Tensorflow
   - Sever: GPUT4
   - Goolge colab

## Dataset
    In this study, the datasets of  human O-linked Threonine Glycosylation (OTG) were collected from HOTGpred [15], DOGpred [17], O-GlyThr [14], UniProt database [23] and relative literatures. After some technical steps to remove redandunt data, we decided to utilize the same dataset as the most recent studies used on human OTG sites prediction, including HOTGpred [15], DOGpred [17], O-GlyThr [14]. This resulted in 318 human OTG proteins. In order to remove duplicate and redundant proteins, the CD-HIT tool [24] was applied with a 40% sequence identity threshold, which refined the dataset to 246 unique human proteins. (Detail dataset in this study in the Table 1).
     
| Dataset | Protein | Positive sites | Negative sites |
|----------|----------|----------|----------|
| Initial dataset   | 318   | 1078   | 110923   |
| Filtered dataset (40% similarity)   | 246   | 1078   | 1078   |
| Training   | -  | 878  | 878  |
| Balanced test  | -  | 200  | 200  |
| Imbalanced test  | -  | 200  | 1000  |


## Train model:
  - Cross validation: CV_DP_OTG.ipynb (10-fold cross validation and search the best model DP_OTG.h5)
  - Model saved and named: DP_OTG.h5. You can use DP_OTG.h5 in the Model folder for predict and independent test.
  - Independent test and predict: DP_OTG_predict.ipynb.

**Contact**: Please feel free to contact us if you need any help: nvnui@ictu.edu.vn

