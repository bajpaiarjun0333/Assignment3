->**Deep Learning Assignment 3- CS6910**
  
  
**List of files in the project:** 
1. train.py
2. readme.md
3. predictions_vanilla
4. predictions_attention


**----------------------------------------------Instructions for running the file:------------------------------------**  

**->The best values of hyperparameters are as follows:**
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

**->Running the file:(No wandb, No argparse)**  
1.) The train.py file is all set to run, to run it kindly run it on kaggle directly and import the dataset.       
2.) The code has been set to take up the best configuration and run.  
3.) The above code is form line 888 till 970  


**->Running the file:(wandb)**  
1.) To run using wandb kindly comment the code at the end, and uncomment the run_sweep() function and also the sweep config and sweep init line.        
2.) We need to also ucomment the lines in run epochs methods which involve wandb.log and wandb.login right at the start      
3.) Comment the code from line 888 to line 970     
4.) Comment the code from line 788 to line 886    
5.) Uncomment the code from line 664 to line 785    


**->Running the file:(argparse)**    
1.) To run using wandb kindly comment the code at the end, and uncomment the lines starting from parser=argparse.parser() till the start of run_sweep() function.   
2.) For running the argparse successfully on the localmachine we need to change the path locations in the load data function.    
3.) Comment the code from line 888 to line 970   
4.) Comment the code from line 664 to line 785  
5.) Uncomment the code from line 788 to line 886
 
############################################################################################

**->Kindly change the path of the dataset in the load data function in order to run the files.**  
