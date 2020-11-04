# Language-Identification-using-WiLI-2018-Dataset

Extracted character based tf-idf features from training data and then trained them on a MLP. Given an unknown paragraph, it predicts the dominant language (among 235 different languages).This dataset consists of short text extracts from Wikipedia. It contains 1000 paragraphs of 235 languages, totaling in 235 000 paragraphs. It is a classification dataset: Given an unknown paragraph, it will predict the dominant language. You can download data from [here](https://zenodo.org/record/841984/files/wili-2018.zip).

Features is extracted using the technique of character-based tf-idf and then MLP classifier is be used to predict the appropriate/dominant language. Before this, the data needs to be cleaned and normalized. Normalization steps include removing punctuation, making the text lowercase or reducing the character set.

Character-based term frequency-inverse document frequency features with a minimum absolute occurrence of 100 times in the training dataset are used. The resulting 2218 features are L2 normalized. A multilayer Perceptron with one hidden layer of 512 neurons followed by the ReLU activation function and an output layer of 235 neurons followed by softmax is used as a classifier. This network has 1,256,683 parameters. The cross-entropy loss function and the Adam optimizer are used. The model is trained for 20 epochs with a mini-batch size of 32.

On the test/validation set, the results which they got are as follows :

    Accuracy (On training data)           : 	92.81%  
    Accuracy (On testing data) 	      : 	89.42% 
    
### Reference:
```
@article{DBLP:journals/corr/abs-1801-07779,
  author    = {Martin Thoma},
  title     = {The WiLI benchmark dataset for written language identification},
  journal   = {CoRR},
  volume    = {abs/1801.07779},
  year      = {2018},
  url       = {http://arxiv.org/abs/1801.07779},
}
```


