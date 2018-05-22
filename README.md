# Linear-Machine-Learning-Algorithms
Implementation of Perceptron, Winnow and Adagrad-Perceptron, along with their averaged versions on synthetic and real world datasets 

# Datasets 

1.  Synthetic Sparse data:  training, development, test.
2.  Synthetic Dense data:  training, development, test.
3.  Real data set:  Training = CoNLL; Dvelopment = CoNLL and Enron; Test:  CoNLLand Enron.
# Running the Script
If you run the main function without doing any changes, you will get the following:

1. News Dev Accuracy For Averaged Perceptron
2. Email Dev Accuracy for Averaged Perceptron 
3. News Dev Accuracy for SVM 
4. Email Dev Accuracy for SVM
5. Accuracies of 7 seven models for sparse and synthetic development data.

*Accuracies are developed after 10 iterations. This is because averaged versions require some catch up with their normal versions.I talk about this in my report.*


# Implementation Details:

The implementation of Adagrad, Winnow and Perceptron are all under Classifier class. 

If averaged variable is True, average versions of the algorithms are implemented. 


\b Other Added Functions that are uncommented in Main Function: \

\b0 \
Developing Accuracy plots is done is done by 
\b plot_learning_curves(x_train,y_train,x_test,y_test) 
\b0 function. To print out the graph, please uncomment these lines: \
\
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f1 \cf2 \cb3 plot_learning_curves\cf4 (syn_dense_train_x, syn_dense_train_y, syn_dense_dev_x, syn_dense_dev_y)\
\cf2 plot_learning_curves\cf4 (syn_sparse_train_x, syn_sparse_train_y, syn_sparse_dev_x, syn_sparse_dev_y)\
\
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f0\b \cf0 \cb1 \

\b0 In order to tune alpha for winnow by plotting different alpha accuracies, you can uncomment the line:\
\
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f1 \cf2 \cb3 tune_alpha_winnow\cf4 (syn_sparse_train_x,syn_sparse_train_y,syn_sparse_dev_x,syn_sparse_dev_y)\
\
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f0 \cf0 \cb1 \
In order to tune eta for Adagrad by plotting different learning rate accuracies, you can uncomment the line:\

\b \
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f1\b0 \cf2 \cb3 tune_eta_adagrad\cf4 (syn_sparse_train_x, syn_sparse_train_y, syn_sparse_dev_x, syn_sparse_dev_y)\
\
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f0 \cf0 \cb1 \
In order to write Average Perceptron and SVM predictions for real test data into a text file, I utilise the 
\b get_predictions_from_real_test_data() 
\b0 function. To see how this function runs you can uncomment certain lines in main function. I commented what each line does similar to this example: \
\
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f1 \cf5 \cb3 # The function writes Average Perceptron Predictions on CoNLL Data to p-connl.txt\
\cf6 """\
get_predictions_from_real_test_data(news_test_x, 'conll', 'Perceptron', avg_p_news)\
"""
\f0 \cf0 \cb1 \
\
In order to write Average Perceptron and SVM predictions for synthetic test data into a text file, I utilise the 
\b get_predictions_from_syn_test_data() 
\b0 function. I call this function for sparse and dense test data. You can uncomment these specified lines in main function to write a text file that will write in your current directory. For me this was the directory where my PyCharm Project was located. \
\
Also when writing to a text file, I had a blank line at the end of each file and I deleted all of them manually. I apologise for any inconvenience. \
I hope this was helpful. Thank you for reading. \
}