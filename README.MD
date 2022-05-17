# Huawei NLP course final project  

This repo contains code for patent phrase to phrase matching task. 
Baseline is one-class classification (in fact regression) with huggingface deberta. 
Trying to beat baseline with finetuning deberta as language model with 2.4 GB patent texts. 
Unfortunately, not done, may be too much garbage in patent texts.  

## Deberta-small baseline 

| Epoch | Training Loss | Validation Loss | Pearson  |
|-------|---------------|-----------------|----------|
| 1     | No log        | 0.022936        | 0.817260 |
| 2     | 0.033200      | 0.020324        | 0.838192 |
| 3     | 0.018600      | 0.020491        | 0.843216 |
| 4     | 0.012100      | 0.020256        | 0.849351 |
| 5     | 0.008700      | 0.019608        | 0.853092 |

## Deberta-small pretrained as language model lr=1e-4

| Epoch | Training Loss | Validation Loss | Pearson  |
|-------|---------------|-----------------|----------|
| 1     | No log        | 0.044398        | 0.586044 |
| 2     | 0.063300      | 0.032534        | 0.722383 |
| 3     | 0.036800      | 0.029753        | 0.749877 |
| 4     | 0.026400      | 0.031267        | 0.756730 |
| 5     | 0.021400      | 0.030229        | 0.761607 |

## Deberta-small pretrained as language model lr=1e-9

| Epoch | Training Loss | Validation Loss |  Pearson |
|------:|--------------:|----------------:|---------:|
|     1 |        No log |        0.025315 | 0.812457 |
|     2 |      0.037100 |        0.021570 | 0.830168 |
|     3 |      0.020100 |        0.020210 | 0.838178 |
|     4 |      0.014600 |        0.020303 | 0.848101 |
|     5 |      0.011500 |        0.020308 | 0.848713 |
