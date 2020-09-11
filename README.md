# WF-ML-BATCH-HACKATHON

# Preprocessing
Pre-processing the data is a time consuming task and and the methodology can be continuously improved. Lemmantizing instead of stemming ensures words are not cut at the beginning/end without any meaning. The lemmantizing process in itself can be improved significantly. Another issue is the check for english words. This is a difficult task and when implemented, will improve the cleanliness of the data. The flow of cleaning the data, that is, removing stopwords, special characters, numbers and hyperlinks should be taken to consideration, since each of these processes can be dependent on each other. For instance, removing special characters before stopwords will result in missing out few stopwords included in the processed data. 

# Vectorization
Even though the difference between count vectorization and TFIDF vectorization is understood, the results produced in this particular case are not very different. This might be due to the sheer large number of features present in the data. 

# Modelling
Random Forest had directly been chosen as the only ensemble algorithm run through gridsearchCV with cross validation. The model was overfitting the training data and performed nominally on testing data. The data was fed to an ANN after this. Softmax activation was choosen for the last layer since it works well for multi class classification. The same reasoning goes for selecting categorical cross entropy as loss function. Adam optimizer performed marginally better than the other optimizers while testing initially. The number of hidden layers and neurons were not varied much since time taken to optimize all combinations of parameters was significant. LSTM analysis was again performed for the same data and again, the model overfitted the training data.

One viable solution to this issue could be to further work on the data cleaning it and spending more time on preprocessing. Another could be in optimizing the parameters for the aformentioned NN's.
