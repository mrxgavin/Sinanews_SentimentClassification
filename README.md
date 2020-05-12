# Sentiment Classification based on Sina News (Final project of NLP2020)

## Environment:
* python >= 3.6
* Pytorch == 1.1.0
* TensorboardX(Visualization)

## Instructions

The main.py in the Code folder is the program entry, run
```
python main.py --config config_path
``` 
 train the specificed model 
```
python main.py --config configs/cnn_with-non-static-w2v.json
```
or run `./code/runall.sh`

## Summary of experimental results

|   Model   | Accuracy(%) | F1(%) | Pearson | Time |                            Parameter configuration                            |
| :------: | :---------: | :---------: | :--: | :--------------: | :--------------------------------------------------------: |
|   MLP   |    53.2     |    21.5     | 0.50 |      4m13s       |     [config/mlp_with-non-static-w2v.json](./config/mlp_with-non-static-w2v.json)     |
|   CNN   |    63.1     |    31.2     | 0.63 |      9m13s       |     [config/cnn_with-static-w2v.json](./config/cnn_with-static-w2v.json)      |
|  LSTM  |    50.5     |    26.2     | 0.48 |      10m47s      | [config/rnn_lstm_with-non-static-w2v.json](./config/rnn_lstm_with-non-static-w2v.json)      |
|  GRU  |    57.6     |    26.3     | 0.40 |      9m43s      | [config/rnn_gru_with-non-static-w2v.json](./config/rnn_gru_with-non-static-w2v.json)      |

The following picture is `CNN train_loss`
![](./report/CNN_train_loss.svg)

To view more charts, you can run the following command to open Tensorboard.
```
tensorboard --logdir runs
```

