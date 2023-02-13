# Bert
# RoBERTa
------
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
