# BiteNet-Reconstruction
CS 598 Deep Learning for Healthcare Final Project

This is code for BiteNet model reconstruction. 

This is original paper: Xueping Peng, Guodong Long, Tao Shen, Sen Wang, Jing Jiang, and Chengqi Zhang. 2020. Bitenet: bidirectional temporal encoder network to predict medical outcomes. In 2020 IEEE International Conference on Data Mining (ICDM), pages 412–421. IEEE.

This is original paper's code: https://github.com/Xueping/BiteNet

It uses python packages numpy, torch and sklearn.

To run this project, first run data_prepare code, then BiteNet code.

In data_prepare code, data are pre-processed. All data used and generated are in data folder. You can run this notebook from start to end to repeat my preparation process.

In BiteNet code, there are 5 parts. First part is loading data from previous preparation. Second part is define BiteNet model. 
Third part is training and predicting with BiteNet. AUC score is printed. Fourth part is training and predicting with baseline models.
Last part is ablation study.
The code can run from start to end to produce my result.

My results of auc score are printed in notebook.

Training code and evaluation code are both in BiteNet notebook. You can refer to bitenet_train and bitenet_test function in part 3.

The training time is relatively short. The model can be trained on personal computer. So we don't provide a pre-trained model. 

Results are as below for comparing BiteNet and baseline models and ablation study.


|Model   |  AUC Score   |
|--------|--------------|
|RNN     |  0.2665      |
|RETAIN  |  0.2744      |
|BiteNet |  0.2967      |


|Model                  |  AUC Score  |
|-----------------------|-------------|
|BiteNet                |  0.2967     |
|BiteNet w/ replacement |  0.2798     |

