# AWS-Certified-Machine-Learning-Study-Notes
AWS Certified Machine Learning – Study Notes

> These notes are written by a data scientist, so some basic topics may be glanced over.

# Learning Path
1. [Linux Academy](https://linuxacademy.com/cp/modules/view/id/340)
2. [Whizlabs Practise exams](https://www.whizlabs.com/aws-certified-machine-learning-specialty/) _(18 September2019:Coming soon)_

# 1. [Machine learning concepts](1-concepts.md)
* Machine learning lifecycle
* Supervised vs Unsupervised vs Reinforcement learning
* Optimisation
* Regularisation (L1 Lasso & L2 Ridge)
* Hyperparameters
* Cross-validation

# 2. [Data](2-data.md)
* Feature selection
* Feature engineering
* Principal Component analysis (PCA)
* Missing and unbalanced data
* Label encoding & One-hot-encoding
* Train-test splits & Randomisation
* RecordIO format

# 3. [Machine learning models](3-machine-learning-models.md) 
* Logistic Regression
* Linear regression 
* SVM
* Decision trees
* Random Forest
* K-means
* KNN
* Latent Dirichlet ALlocation - LDA

# 4. [Deep Learning](4-deep-learning.md)
* Neural Networks
* Activations functions (sigmoid, Tanh, ReLU)
* Weights & biases
* Forward & Back propogation
* Convolutional Neural Networks (CNN)
* Filters
* Transfer Learning
* Recurrent Neural Networks (RNN)

# 5. [Model Performance and Optimization](5-model-performance.md)
* Sensitivity (Recall / TPR)
* Specificity (TNR)
* Precision
* Accuracy
* ROC / AUC
* F1 Score
* Gini impurity

# 6. [Machine Learning Tools and Frameworks](6-tools-frameworks.md)
* Pytorch & Scikit-learn
* Tensorflow & Keras
* MXNET & Gluon
* Tensors & Graphs

# 7. [AWS Services](7-aws-services.md)
* S3 Datalakes
* Kinesis (video stream / data stream / firehose / data analytics)
* Glue 
* Athena
* Elastic Map Reduce (EMR) & Spark
* EC2 instance types for ML
* AWS Machine Learning service (deprecate)

# 8. [AWS Application Services AI/ML](8-aws-applications-ai-ml.md)
* Rekognition (images)
* Rekognition (videos)
* Polly (text2speech) 
* Transcribe (speech2text)
* Translate
* Comprehend
* Lex (chatbots)
* Step Functions

# 9. Sagemaker -- VERY IMPORTANT TOPIC
## [Intro](9a-sage-intro.md)
* Sagemaker High Level
* Three stages: Build, train, deploy
* Sagemaker console
* Sagemaker API
* Sagemaker Python SDK

## [Sagemaker Build](9b-sage-build.md)
* **!!Define your problem first!!**
* **Build process**: Visualise, Explore, Feature engineering, Synthesize data, Convert data, Change structure (joins), Split data
* Ground truth
* **SageMaker Algorithms**: Built in, marketplace, custom
* **Algorithm Types**: eg. BlazingText (AWS-Comprehend), Image classification (AWS-Rekognition)
