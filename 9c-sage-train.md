# Sagemaker Train

## Sagemaker architecture for training
When you start a sagemaker training job AWS calls ECS and the containers that contain the algorithms. We also need data, generally stored in S3. 
* We define the algorithms and where the data lives
* Sagemaker then spins up the EC2 instances it needs, pulls in the data, trains the model using the models available in ECS. 

**AWS Marketplace**: **Algorithms** are to be trained, **Model packages** are pre-trained

**Where to access data**: S3, EFS, FSx for Lustre (High performance, high throughput for High Performance Computing -- HPC)

**Filetypes**: Files / Pipe (recordIO)

Instance types
* Some algorithms only support GPU instances (ml.p2 family)
* AWS recommends: ml.m4, ml.c4, ml.p2 (GPU)
* GPUs more expensive, but faster

**Managed spot training**: Optimise cost of training models up to 90% over on-demand using spot instances, using **Sagemaker Checkpoints** in the model state

## Hyperparameter tuning
Choose model, set ranges of hyperparameters (max_depth:3-9), choose performance metric to measure (maximise AUC)
* There's a machine learning model, that monitors which hyperparameters are working the best and tunes the models accordingly. 
