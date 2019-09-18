# AWS-Certified-Machine-Learning-Study-Notes
AWS Certified Machine Learning – Study Notes

> These notes are written by a data scientist, so some basic topics may be glanced over 

# Learning Path
1. [Linux Academy](https://linuxacademy.com/cp/modules/view/id/340)
2. [SageMaker FAQ](https://aws.amazon.com/sagemaker/faqs/)
3. Practise exams
    * [Udemy practise exams (£20)](https://www.udemy.com/course/aws-machine-learning-practice-exam/?couponCode=MLPRACTICE) 
    * [Whizlabs Practise exams _(£29 - Coming soon)_](https://www.whizlabs.com/aws-certified-machine-learning-specialty/)
    * 

Below is a high level overview. More in-depth explanations are found in separate files

# 1. [Machine learning concepts](01-concepts.md)
* Machine learning lifecycle
* Supervised vs Unsupervised vs Reinforcement learning
* Optimisation
* Regularisation (L1 Lasso & L2 Ridge)
* Hyperparameters
* Cross-validation

# 2. [Data](02-data.md)
* Feature selection
* Feature engineering
* Principal Component analysis (PCA)
* Missing and unbalanced data
* Label encoding & One-hot-encoding
* Train-test splits & Randomisation
* RecordIO format

# 3. [Machine learning models](03-machine-learning-models.md) 
* Logistic Regression
* Linear regression 
* SVM
* Decision trees
* Random Forest
* K-means
* KNN
* Latent Dirichlet ALlocation - LDA

# 4. [Deep Learning](04-deep-learning.md)
* Neural Networks
* Activations functions (sigmoid, Tanh, ReLU)
* Weights & biases
* Forward & Back propogation
* Convolutional Neural Networks (CNN)
* Filters
* Transfer Learning
* Recurrent Neural Networks (RNN)

# 5. [Model Performance and Optimization](05-model-performance.md)
* Sensitivity (Recall / TPR)
* Specificity (TNR)
* Precision
* Accuracy
* ROC / AUC
* F1 Score
* Gini impurity

# 6. [Machine Learning Tools and Frameworks](06-tools-frameworks.md)
* Pytorch & Scikit-learn
* Tensorflow & Keras
* MXNET & Gluon
* Tensors & Graphs

# 7. [AWS Services](07-aws-services.md)
* S3 Datalakes
* Kinesis (video stream / data stream / firehose / data analytics)
* Glue 
* Athena
* Elastic Map Reduce (EMR) & Spark
* EC2 instance types for ML
* AWS Machine Learning service (deprecate)

# 8. [AWS Application Services AI/ML](08-aws-applications-ai-ml.md)
* Rekognition (images)
* Rekognition (videos)
* Polly (text2speech) 
* Transcribe (speech2text)
* Translate
* Comprehend
* Lex (chatbots)
* Step Functions

# 9. Sagemaker -- VERY IMPORTANT TOPIC
## [Intro](09a-sage-intro.md)
* Sagemaker High Level
* Three stages: Build, train, deploy
* Sagemaker console
* Sagemaker API
* Sagemaker Python SDK

## [Sagemaker Build](09b-sage-build.md)
* **!!Define your problem first!!**
* **Build process**: Visualise, Explore, Feature engineering, Synthesize data, Convert data, Change structure (joins), Split data
* Ground truth
* **SageMaker Algorithms**: Built in, marketplace, custom
* **Algorithm Types**: eg. BlazingText (AWS-Comprehend), Image classification (AWS-Rekognition)

## [Sagemaker Train](09c-sage-train.md)
* Architecture behind Sagemaker training: Algorithms stored in docker containers in ECS, spin up EC2 instances
* **AWS Marketplace**: **Algorithms** are to be trained, **Model packages** are pre-trained
* **Where to access data**: S3, EFS, FSx for Lustre 
* **Filetypes**: Files / Pipe (recordIO)
* **Instance types**: ml.m4, ml.c4, ml.p2 (gpu)
* Some algorithms only support GPU instances
* Managed spot training & Checkpoints
* Automated Hyperparameter tuning

## [Sagemaker Deploy](09d-sage-deploy.md)
* Real-time inference
* Batch inference

# 10. [Security](10-security.md)
* Sagemaker root access
* **AmazoneSageMakerFullAccess** policy: Admin access to SageMaker + necessary access to other services
* Sagemaker can see objects in S3 by default, can't access
* Deployed into **public VPC** by default

# Other 
* **AWS DeepLens** – Deep learning enabled video camera for developers
* **AWS DeepRacer** - Reinforcement learning enabled race-car 

## Sagemaker FAQs notes
* **CloudTrail** to see SageMaker API calls
* **Notebooks persist** on the volume of the attached instance. So stopping the instance doesn't make you lose your progress.
* **Managed spot training** uses Spot instance to train. Have to specify time to wait for spot capacity
    * Good when you have flexibility
    * Uses checkpoints to store progress. Avoids failure when instance is terminated. 
* BlazingText
* **Automated hyperparameter tuning** available for all algorithms (including custom one).
    * Uses a custom Bayesian Optimization under the hood
* Can currently only optimise for one objective (ie. accuracy or speed)
* **Reinforcement learning** is a machine learning technique that enables an agent to learn in an interactive environment by trial and error using feedback from its own actions and experiences
    * Available to train in SageMaker. Can use **AWS RoboMaker**, Open AI Gym or commercial simulation environments to train 
* **SageMaker Neo**: Enables machine learning models to train once and run anywhere in the cloud and at the edge
    * Optimizes models built with popular deep learning frameworks that can be used to deploy on multiple hardware platforms
    * Two major components – a **compiler** and a **runtime**
    * Supports the most popular deep learning models for computer vision and decision tree models: 
        * AlexNet, ResNet, VGG, Inception, MobileNet, SqueezeNet, and DenseNet models trained in MXNet and TensorFlow, 
        * classification and random cut forest models trained in XGBoost
* Model performance from multiple runs is available in the Management Console in tabular form giving you a **leaderboard**
* Can't directly access the underlying hardware SageMaker runs on
* Can scale manually, or automatically using **Application Auto Scaling**
* **CloudWatch Metrics** to monitor SageMaker environment 
    * Logs written to CloudWatch

## SageMaker Algorithms - Overview
* **Built-in algorithms**: 
    * linear regression
    * logistic regression 
    * k-means clustering
    * principal component analysis (PCA)
    * factorization machines
    * neural topic modeling 
    * latent dirichlet allocation
    * gradient boosted trees
    * sequence2sequence
    * time series forecasting
    * word2vec
    * image classification
* **Optimized containers**: 
    * Apache MXNet
    * Tensorflow
    * Chainer
    * PyTorch
* **Custom algorithms** by using Docker images
