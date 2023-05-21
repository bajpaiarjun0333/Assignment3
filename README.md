Deep Learning Assignment 3- CS6910
List of files in the project: 
1. train.py
2. readme.md
3. predictions_vanilla
4. predictions_attention

Instruction to run the project:
1. With wandb:
Kindly uncomment the following piece of code:
# def runSweep():
#     #default for sweep
#     config_defaults = {
#         "es": 64,
#         "nle": 3,
#         "nld": 3,
#         "hs": 256,
#         "ct": "LSTM",
#         "bi": True,
#         "de": 0.2,
#         "dd": 0.3,
#         "ep": 20,
#         "bs": 128,
#         "attention":False,
#         }
    
#     wandb.init(project = 'Assignment3', entity = 'cs22m020', config=config_defaults)
#     es = wandb.config.es
#     nle = wandb.config.nl
#     nld = wandb.config.nl
#     hs = wandb.config.hs
#     bs = wandb.config.bs
#     ep = wandb.config.ep
#     ct = wandb.config.ct
#     bi = wandb.config.bi
#     de = wandb.config.de
#     dd = wandb.config.dd
#     attention=wandb.config.attention
    
#     alpha = 0.001
    
#     params={"hs":hs,
#             "nl":nle,
#             "de":de,
#             "dd":dd,
#             "bs":bs,
#             "es": es,
#             "ep":ep,
#             "ct":ct,
#             "alpha":alpha,
#             "bi":bi,
#             "attention":attention
#             }
    
#     eng=Dictionary(max_inp_len)
#     hin=Dictionary(max_out_len)
#     train_batch_input=eng.driver(train_input,params["bs"])
#     train_batch_target=hin.driver(train_output,params["bs"])
#     valid_batch_input=eng.driver(valid_input,params["bs"])
#     valid_batch_output=[]

#     #go over the validation output and convert to batches
#     for i in range(0,len(valid_output),params["bs"]):
#         if i+params["bs"]>=len(valid_output):
#             break
#         temp=[]
#         for j in range(i,i+params["bs"]):
#             temp.append(valid_output[j])
#         valid_batch_output.append(temp)


#     train_actual_output=[]
#     for i in range(0,len(train_output),params["bs"]):
#         if i+params["bs"]>=len(train_output):
#             break
#         temp=[]
#         for j in range(i,i+params["bs"]):
#             temp.append(train_output[j])
#         train_actual_output.append(temp)
    
    
#     if attention==False:
#         encoder1 = Encoder(eng.n_chars, params).to(device)
#         decoder1 = Decoder(params, hin.n_chars).to(device)
#         Combine(encoder1, decoder1, ep, alpha, bs, es, ct, train_batch_input, train_batch_target, valid_batch_input,valid_batch_output,hin, nld,nle,dd,de,train_actual_output,hs,bi)
#     else:
#         encoder1 = EncoderAttention(eng.n_chars, params).to(device)
#         decoder1 = DecoderAttention(params, hin.n_chars).to(device)
#         CombineAttention(encoder1, decoder1, ep, alpha, bs, es, ct, train_batch_input, train_batch_target, valid_batch_input,valid_batch_output,hin, nld,nle,dd,de,train_actual_output,hs,bi)


##################################################################################################################################################

# sweep_config = {
#   "name": "Recurrent Neural Network - Cross Entropy Loss",
#   "metric": {
#       "name":"validation_accuracy",
#       "goal": "maximize"
#   },
#   "method": "bayes",
#   "parameters": {
#         "es": {
#             "values": [512, 256, 64, 32]
#         },
#         "nl": {
#             "values": [3, 2, 1]
#         },
#         "hs": {
#             "values": [512, 256, 128]
#         },
#         "ct": {
#             "values": ["RNN", "GRU", "LSTM"]
#         },
#         "bi": {
#             "values": [False, True]
#         },
#         "de": {
#             "values": [0.2, 0.3, 0.4]
#         },
#         "dd": {
#             "values": [0.2, 0.3, 0.4]
#         },
#         "ep": {
#             "values": [20, 30]
#         },
#         "bs": {
#             "values": [256, 128, 64, 32]
#         },
#         "attention": {
#             "values": [False,True]
#         }
#     }
# }
# sweep_id = wandb.sweep(sweep_config, entity="cs22m020", project="Assignment3")
# wandb.agent(sweep_id, runSweep, count = 2)
#running the sweep functionality


2. To run without wandb: This is the default mode
Kindly comment out the wandb code stated above, and run the file and pass the arguments from the command line.\

