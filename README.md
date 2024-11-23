# Language-Model-Efficiency-Challenge
The challenge of training and evaluating an LLM under tight computational constraints that mirror real-world limitations will be tackled.

## Execution Instructions
Suppose you do not have the optim hyperparameters:
1. Clone the repository
2. Run if wanted the file 'optuna_OASST1_1param.ipynb' to obtain the optimized hyperparameters of the model, and change the hyperparameters in the file 'train_def_dataset1.ipynb'.
3. Run the file 'train_def_dataset1.ipynb' to train the model
4. Run the file 'optuna_ifeval_like_dataset.ipynb' to optimize the hyperparameters of the trained mode and change the hyperparameters in the file 'train_def_dataset2.ipynb'.
5. Run the file 'train_def_dataset2.ipynb' to train the model
6. Run nlpifeval.ipynb and when finished, execute on the terminal the command in the ifeval_command.txt

The other files were used to test the model and to understand the data.


Useful link:
This link contains different folders. 'data' includes jsonl files with answers to evaluate IfEval. The best accuracy is obtained with: 
The model_ folders are different checkpoints of the model.
https://upcomillas-my.sharepoint.com/:f:/g/personal/202106145_alu_comillas_edu/Emxrq9iIW39CpfTp2K4kjyUB7Z5mcklC25xHuU5we3CAlA?e=XR5uLj