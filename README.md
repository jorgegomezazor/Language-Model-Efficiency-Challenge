# Language-Model-Efficiency-Challenge
This repository contains the implementation of the 1 Model, 1 GPU, 1 Day: Language Model Efficiency Challenge, developed for the Natural Language Processing II (2024/2025) course. The goal of this project is to explore and optimize fine-tuning techniques for language models under strict computational constraints.

Project Objective
Train and evaluate a pre-trained language model (LLM) through Supervised Fine-Tuning (SFT) within a maximum of 24 hours, using a single GPU (Nvidia 4070 Ti with 12 GB of RAM).

This project addresses the challenge of balancing model size, data quality, and optimization techniques to achieve the best performance within available resource limits.

## Repository Structure

### **Directories**
- `ifeval/`: Resources for IFEval, the evaluation benchmark used for model performance. It contains:
    - `human_ifeval_OASST1.ipynb`: notebook used to evaluate visually in a certain moment the responses that the model generates for the IfEval prompts. Used in the preliminary process.
    - `ifeval_command.txt`: contains command to execute in the terminal, when IfEval benchmarks want to be evaluated.
    - `nlp_ifeval.ipynb`: notebook used to evaluate models with IfEval benchmarks.

- `instruction_following_eval/`: Scripts used to evaluate the prompts produced in nlp_ifeval.ipynb.
- `optuna/`: Contains the notebooks used to optimize the hyperparameters of the model.
    - `optuna_OASST1_1param.ipynb`: notebook used to optimize the hyperparameters of the model.
    - `optuna_OASST1_3params.ipynb`: notebook used to optimize the 3 hyperparameters of the model at the same time.
    - `optuna_ifeval_like_dataset.ipynb`: notebook used to optimize the hyperparameters of the model after executing the first training phase of the model.
- `screenshot/`: Contains screenshots of IfEval benchmarks.
### **Files**
- `performance_dataset1.ipynb`: notebook used after training with the first dataset, to evaluate the performance of the model with benchmarks of the model.
- `performance_dataset2.ipynb`: notebook used after training with the second dataset, to evaluate the performance of the model with benchmarks of the model.
- `train_def_dataset1.ipynb`: notebook used to train the model with the first dataset.
- `train_def_dataset2.ipynb`: notebook used to train the model with the second dataset.


## Execution Instructions
Suppose you do not have the optim hyperparameters:
1. Clone the repository
2. Run if wanted the file 'optuna_OASST1_1param.ipynb' to obtain the optimized hyperparameters of the model, and change the hyperparameters in the file 'train_def_dataset1.ipynb'.
3. Run the file 'train_def_dataset1.ipynb' to train the model
4. Run the file 'optuna_ifeval_like_dataset.ipynb' to optimize the hyperparameters of the trained mode and change the hyperparameters in the file 'train_def_dataset2.ipynb'.
5. Run the file 'train_def_dataset2.ipynb' to train the model
6. Run nlp_ifeval.ipynb and when finished, execute on the terminal the command in the ifeval_command.txt

Useful link:
https://upcomillas-my.sharepoint.com/:f:/g/personal/202106145_alu_comillas_edu/Emxrq9iIW39CpfTp2K4kjyUB7Z5mcklC25xHuU5we3CAlA?e=XR5uLj
This link contains different folders. 'data' includes jsonl files with answers to evaluate IfEval. The best accuracy is obtained with the IfEval responses in the file 'data/input_response_data_2_128.jsonl'. However, as stated in the report, for our visual evaluation, we prefer using the responses from 'data/input_response_data_2_512.jsonl', as their accuracies are very similar.  It has to be included in 'instruction_following_eval/data' with the name 'input_response_data.jsonl'.
The model_ folders are different checkpoints of the model.