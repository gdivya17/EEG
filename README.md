CLASSIFICATION OF EMOTIONS BY ANALYZING EEG SIGNALS 

The project was carried out to perform analysis of EEG signals to classify the emotions of 32 subject using signal processing and machine learning techniques.

Utilities [Util colab notebook](https://colab.research.google.com/drive/1-2NY0DhOIePT5tpD24GynwKgbaaUJZSH):
1) Decomposing of all 32 subject files [original dat files](https://drive.google.com/drive/folders/1zxLqJBKz8I5zs4M3uur-nQDckeTlPbi0) into 10 subbands using empirical wavelet transform [final_h5 files](https://drive.google.com/drive/folders/1Kk6_feIkc7HM2R_ydhMTLsnj_CuVHYrA).
2) For feature extraction purposes we used a time series of resultant subbands that calculated 5 different entropies [subjectwise_entropies](https://drive.google.com/drive/folders/1xRzUcvtVvH7QgjG-zPB1kO7hcBOTs_1s).
3) Then concatenated each entropy file and got a 2d matrix for better computation and for feasibility of analysis of dataset [entropies combined](https://drive.google.com/file/d/11AbX-et7py0eoG063OGB99vEDKQSpTAh/view).
4) Dividing combined entropy file into 10 files for each subband [bandwise entropies](https://drive.google.com/drive/folders/1U718poZGFw-GsVNmGGHE666GR6mRL6vb).
5) Then for computation purposes we oversampled label class as final label [labels used](https://drive.google.com/drive/folders/1UAYtZZIU8qckBNGJYV4meNXVDXENz-A-).

Final Classification (Classification colab notebook):
1) To improve data integrity we performed oversampling in 0’s and 1’s as the output is bias
toward 1’s we oversampled 0’s in the training dataset thus without the loss of information
we get the model trained.
2) After classification with 5 models we choose top 3 model which are giving us better
results then others and take mode of prediction and then calculate the accuracy.
