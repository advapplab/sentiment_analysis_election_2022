# sentiment_analysis_election_2022

## Instructions

update 6/12: We now also have a version that can directly predict the sentiment for unlabelled data. See: predict_unlabelled_data.ipynb 


If you want to run data where the labels are stored in the column 'sentiment', please run weibo_wmmBERT_testing_6.ipynb.<br>
If you want to run data where the labels are stored in the column 'cya_check_3', please run  weibo_wmmBERT_testing_Cya_check_3.ipynb.<br>
The code automatically selects the labels it needs (positive/negative) and ignores the rest.

The code is currently set to import df_sample.xlsx, but feel free to change it to the excel sheet with the new data once you have it. In order
to do this you will have to: 
1. upload a new excel file under data/challange.
2. change the link in the code in cell 4 and cell 7. 
    
The easiest way to run the code directly is to install the chrome extension 'open in colab'. This allows you to open any code on Github directly into
your colab. 

If you have any questions, feel free to contact me on Line. 

## Folder Structure

```
    .
    ├── ...
    ├── data                    
    │   ├── challange                     # ICI dataset
    │   ├── eval                          # Weibo dataset for evaluation
    │   ├── test                          # Weibo dataset for testing
    │   ├── train                         # Weibo dataset for training
    ├── weibo_wmmBERT.ipynb               # Finetuning process to build weibo_wmmBERT (2/6) on wmmBERT pretrain model
    ├── weibo_wmmBERT_testing_6.ipynb     # Evaluate classification accuracy of ICI dataset by weibo_wmmBERT (2/6)
```


## Model Spec

We have aggragated some classes in the Weibo dataset into 'Positive' and 'Negative'. The current spec will be:

|  Original Class   | Aggregated Class  | 
|  ----  | ----  |
|  Angry | Negative |
|  Fear | Negative |
|  Sad | Negative |
|  Happy | Positive |
|  Suprise | Ignore |
|  Neutral | Ignore |

## Model Repositories

2-Classes: https://huggingface.co/owen198/weibo-wmmbert-2

6-Classes: https://huggingface.co/owen198/weibo-wmmbert-2
