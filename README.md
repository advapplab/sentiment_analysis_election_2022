# sentiment_analysis_election_2022

## Folder Structure

```
    .
    ├── ...
    ├── data                    
    │   ├── challange                     # ICI dataset
    │   ├── eval                          # Weibo dataset for evaluation
    │   ├── test                          # Weibo dataset for testing
    │   ├── train                         # Weibo dataset for training
    ├── weibo_wmmBERT.ipynb               # Finetuning process to build weibo_wmmBERT, within 6 classes and wmmBERT pretrain model
    ├── weibo_wmmBERT_testing_6.ipynb     # Evaluate classification accuracy of ICI dataset by weibo_wmmBERT within 6 classes
```


## Model Spec

To improve the classification accuracy on ICI election dataset, we have a meeting at 16:00, 23th Nov. We agree to aggragate some classes in Weibo dataset into 'Positive' and 'Negative'. The current spec will be:

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
