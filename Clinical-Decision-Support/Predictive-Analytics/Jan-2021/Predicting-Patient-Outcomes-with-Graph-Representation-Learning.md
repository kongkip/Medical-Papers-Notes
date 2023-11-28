# Predicting Patient Outcomes with Graph Representation Learning

This paper by Emma Rocheteau, Catherine Tong, Petar Velickovic, Nicholas Lane, and Pietro Liò, focuses on the prediction of patient outcomes in Intensive Care Units (ICU) using a novel approach that combines Long Short-Term Memory networks (LSTMs) and Graph Neural Networks (GNNs).

## Key Points of the Paper:
### 1. Background and Motivation
- ICU patient outcome has traditionally focused on physiological time series data, often overlooking sparse data like diagnoses and medications.
- Current models struggle with rare disease patterns due to their data processing methods.
- The authors took an inspiration from clinicians who tend to rely on their past experience of treating similar patients when making clinical judgements.
- They capture this similarity concept by constructing a patient graph where the nodes are patients and edges express relatedness in diagnoses.  

### 2. Proposed Solution - LSTM-GNN:
- The authors proposed an LSTM-GNN hybrid model. LSTMs extract temporal features, while GNNs handle patient neighbourhood information based on diagnoses.
- This approach aims to laverage diagnoses as relational information, connecting similar patients in a graph, thereby enhancing the prediction accuracy.

### 3. Methodology:
- The model constructs a patient graph with nodes representing patients and edges expressing relatedness in diagnoses.
- The LSTM-GNN operates on this graph, encoding both temporal and graph-based features, which are then used for predicitons.

### 4. Data and Performance:
- The model was trained and evaluated using the eICU database, focusing on in-hospital mortality and length of ICU stay.
- Results indicated that LSTM-GNN outperforms LSTM-only models,especially in predicting the length of stay. This suggests that information from neighbouring patient cases enhances predictive performance.

### 5. Discussion and implications:
- The approach is particularly effective for the length of stay predicitons, higlighthing the benefit of considering diagnoses and patient similarities.
- This method can be extended to other sparse medical data, like shared medications, offering a broader application scope.

### Future Work:
- The paper suggests potential extensions like incorporating shared medications and procedures into the similarity scores.
- It also discusses the need for futher investigation into the sensitivity of the model to various parameters. 

[Paper Link](https://arxiv.org/pdf/2101.03940.pdf)
[Original Authors Implementation](https://github.com/EmmaRocheteau/eICU-GNN-LSTM) 
