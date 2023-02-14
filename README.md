# Bert
# RoBERTa
------
### introduction  
Improve bert model  
1. Increase the training data set   
2. Dynamic mask  
Each time the training example is fed to the model, the mask sentence is randomized, (static masking) the training data is copied to k copies, and a different mask can be fed to the model for each sentence  
3. No NSP and input format (NSP=Next Sentence Predict)   
Simply put, remove the NSP
4. Text encoding  
Bert: character-level vocab 30k  
RoBERTa: byte BPE 50K (use byte, Use bytes instead of unicode characters)

&nbsp;&nbsp;&nbsp;&nbsp; 
<table>
  <tr>
    <td>BERT #params</td>
    <td>RoBERTa #params</td>
  </tr>
  <tr>
    <td>125M</td>
    <td>355M</td>
  </tr>
</table>   

--------

### Experiment 1
* task  
Sentiment analysis, classify dataset text as positive, negitive, neutral
* dataset  
AXS_data_3class_v10.csv
* model  
RoBERTa-Base
* hyperparameter  
iter = 1750  
batch size = 8    
learning rate = 1e-5  
Max_len = 256
* result  
&nbsp;&nbsp;&nbsp;&nbsp; 
F1-score on the test set
<table>
  <tr>
    <td>micro-F1</td>
    <td>macro-F1</td>
  </tr>
  <tr>
    <td> 76.5% </td>
    <td> 72% </td>
  </tr>
</table>   

------

### Experiment 2
* task  
Sentiment analysis, classify dataset text as positive, negitive, neutral
* dataset  
AXS_data_3class_v10.csv
* model  
RoBERTa-Base
* hyperparameter  
iter = 4000
batch size = 8   
learning rate = 1e-5  
Max_len = 256
* result  
&nbsp;&nbsp;&nbsp;&nbsp; 
F1-score on the test set
<table>
  <tr>
    <td>micro-F1</td>
    <td>macro-F1</td>
  </tr>
  <tr>
    <td> 71.25% </td>
    <td> 68.6% </td>
  </tr>
</table>   

--------

### Experiment 3
* task  
Sentiment analysis, classify dataset text as positive, negitive, neutral
* dataset  
AXS_data_3class_v10.csv
* model  
RoBERTa-large
* hyperparameter  
iter = 1750
batch size = 8  
learning rate = 1e-5  
Max_len = 256
* result  
&nbsp;&nbsp;&nbsp;&nbsp; 
F1-score on the test set
<table>
  <tr>
    <td>micro-F1</td>
    <td>macro-F1</td>
  </tr>
  <tr>
    <td> 68.3% </td>
    <td> 66.2% </td>
  </tr>
</table>   
