# Requirements
- `3.6.1 <= python <= 3.8.x`
- `torch == 1.5.1`
- `scikit-learn == 1.0.2`
- `tqdm == 4.63.0`
- `pandas == 1.0.5`
- `pytorch-crf == 0.7.2`

# Running the Binary Classification Model
```
python bin_classifier.py -conf conf/bin/cnn.json -save true
python bin_classifier.py -conf conf/bin/cnn_rnn.json -save true
python bin_classifier.py -conf conf/bin/rnn_cnn.json -save true
python bin_classifier.py -conf conf/bin/rnn.json -save true
```

# Running the Named Entity Recognition Model
```
python ner_classifier.py -conf conf/ner/cnn.json -save true
python ner_classifier.py -conf conf/ner/cnn_rnn.json -save true
python ner_classifier.py -conf conf/ner/rnn_cnn.json -save true
python ner_classifier.py -conf conf/ner/rnn.json -save true
```

# Running the Multi-task Model
```
python mt_classifier.py -conf conf/mt/cnn.json -save true
python mt_classifier.py -conf conf/mt/cnn_rnn.json -save true
python mt_classifier.py -conf conf/mt/rnn_cnn.json -save true
python mt_classifier.py -conf conf/mt/rnn.json -save true
```

# Finding Model Results
All model results will be stored in `ckpts`. `bin` corresponds to the binary classifier,
`ner` corresponds to the named entity recognition model, and `mt` corresponds to the
multi-task model.

# Running Grid Search
Running grid search will take an extremely long amount of time. Results for grid search
will be stored in `results`. If the folder does not exist, run the script and the folder
will be created automatically.

```
python grid_search.py -task bin -arch cnn
python grid_search.py -task bin -arch cnn_rnn
python grid_search.py -task bin -arch rnn_cnn
python grid_search.py -task bin -arch rnn

python grid_search.py -task ner -arch cnn
python grid_search.py -task ner -arch cnn_rnn
python grid_search.py -task ner -arch rnn_cnn
python grid_search.py -task ner -arch rnn

python grid_search.py -task mt -arch cnn
python grid_search.py -task mt -arch cnn_rnn
python grid_search.py -task mt -arch rnn_cnn
python grid_search.py -task mt -arch rnn
```
