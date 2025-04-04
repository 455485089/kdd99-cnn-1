# kdd99-cnn-1
Intrusion Detection Based on Convolutional Neural Network with Kdd99 Data Set

tensorflow：1.12
python：3.6

### Schematic Diagram
Intrusion detection architecture：

![fig1](https://github.com/dendyikbc/kdd99-cnn-1/blob/master/fig1.png)

An example of data processing for KDDCUP.99 data set：

![fig2](https://github.com/dendyikbc/kdd99-cnn-1/blob/master/fig2.png)

The basic structure of the convolutional network：

![fig3](https://github.com/dendyikbc/kdd99-cnn-1/blob/master/fig3.png)



### Source code description

`handle5label.py` is the source code to process train data(`kddcup.data_10_percent_corrected`) & test data(`corrected`).

data set download link：[KDD Cup 1999 Data](http://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html).

`cnn_5label.py`is the source code to train CNN.

`cnn_test5_label.py`is the source code to test CNN，and count and output each type of classification and fuzzy matrix, in the form as follow:![一次结果](https://github.com/dendyikbc/kdd99-cnn-1/blob/master/一次结果.JPG)

maybe the matrix or CNN  was confused, so i called it confused matrix, not fuzzy matrix in code.

and u need  to take some concentrated  time to adjust the parameters of the model to solve the problem about imbalance in kdd99 data set. the former result is adjusted by simple oversampling and downsampling. there is a better one in test:

![MATRIX](https://github.com/dendyikbc/kdd99-cnn-1/blob/master/MATRIX.JPG)



there are something wrong in kdd99 data set，just like the place marked by red circle. `http` is true,not `icmp`. u can find some other problem by `handle5label.py`

![捕获](https://github.com/dendyikbc/kdd99-cnn-1/blob/master/捕获.JPG)
