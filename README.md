Deep Learning Assignment 3- CS6910
List of files in the project: 
1. train.py
2. readme.md
3. predictions_vanilla
4. predictions_attention


Instructions for running the file:

->The best values of hyperparameters are as follows:
hidden size: 512
embedding size: 512
number of layer in encoder: 1
number of layer in decoder: 1
dropout encoder: 0.2
dropout decoder: 0.4
attention: True
bidirectional: False
epochs: 15
learning rate(alpha): 0.001

->Running the file:(No wandb, No argparse)
The train.py file is all set to run, to run it kindly run it on kaggle directly and import the dataset. 
The code has been set to take up the best configuration and run.

->Running the file:(wadb)
To run using wandb kindly comment the code at the end, and uncomment the run_sweep() function and also the sweep config and sweep init line.
We need to also ucomment the lines in run epochs methods which involve wandb.log and wandb.login right at the start

->Running the file:(argparse)
To run using wandb kindly comment the code at the end, and uncomment the lines starting from parser=argparse.parser() till the start of run_sweep() function.
For running the argparse successfully on the localmachine we need to change the path locations in the load data function.

############################################################################################

->Kindly change the path of the dataset in the load data function in order to run the files.
