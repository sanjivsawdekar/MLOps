**Amazon SageMaker**

Basic mlops flow-

<img src="media/image1.png" style="width:6.26806in;height:4.68333in" />

Amazon SageMaker provides below services-

<img src="media/image2.png" style="width:6.26806in;height:4.375in" />

SageMaker allows us to run the different containers on ML-optimized
instances.

The automation tools in AWS **SageMaker Studio** help users to
automatically debug, manage and track ML models. These SageMaker tools
include the following:

**Autopilot** enables AI models to be trained for a given data set and
ranks each algorithm by accuracy. No need to explicitly specify the
model.

**Clarify** flags potential bias that could skew ML models.

**Data Wrangler** is used to speed up data preparation.

**Debugger** monitors the metrics of neural networks to simplify the
debugging process.

**Edge Manager** extends ML monitoring and management to edge devices.

**Experiments** makes it easier to track different ML iterations,
including how changes degrade or improve a model's accuracy.

**Ground Truth** speeds up data labeling and helps to lower labeling
costs when processing large AI training samples. You can label Image,
Text, Video or Custom.

Image: Suported Tasks

<img src="media/image3.png" style="width:1.91in;height:2.31in" />

**JumpStart** offers a set of customizable, predesigned AWS
CloudFormation templates.

**Model Monitor** is an AWS-enabled ML tool to spot application-level
deviations that negatively affect the accuracy of predictions.

**Notebook** creates Jupyter notebooks with one click and transfers the
content of a notebook for collaborative use.

<img src="media/image4.png" style="width:6.26806in;height:1.22569in" />

<img src="media/image5.png" style="width:6.26806in;height:2.10139in" />

You can reuse SageMaker Examples. Just click on Use to create copy of
example notebook. AWS SageMaker Examples GitHub Repository -
<https://github.com/aws/amazon-sagemaker-examples>

<img src="media/image6.png" style="width:6.26806in;height:1.87639in" />

**Pipelines** offer developers ML services for continuous delivery and
continuous integration.

**AWS Marketplace** find & buy readily available trained model developed
by third party vendors, a B2B marketplace.

<img src="media/image7.png" style="width:6.26806in;height:3.52569in" />  
**Training** creates training job on data specified by S3 bucket & place
trained model back in S3 bucket. You can leverage built-in algorithms or
BYO or get once from Marketplace.

Endpoint puts trained model on CPU/GPU to make predictions. You need to
create endpoint before deploying the model to SageMaker.

**Augmented AI ???**

**Lambda** FaaS i.e. serverless computing, upload a code & choose an
event when that code should run. Pay for the exact computing time you
use. For our MLOps pipeline, Lambda functions can be efficiently
leveraged to trigger the different SageMaker jobs (e.g. Train, Evaluate,
Deploy…), perform additional operations if necessary, and pass
parameters (variables passed via CodePipeline) from one step to another
within the pipeline.

**Ec2** (Elastic Compute Cloud) a virtual server, it is like a virtual
computer in cloud, choose OS Memory & computing power & rent that space
in cloud like renting an apartment.

**Docker** containers allows model to run on multiple clouds or
computing environments.

**S3** (Simple Storage Service) stores any type of files. It is nothing
but a simple folder which holds files.

<img src="media/image8.png" style="width:6.26806in;height:1.39653in" />

<u>Writing & listing train & validation datasets to S3 bucket-</u>

<img src="media/image9.png" style="width:6.26806in;height:1.93264in" />

**IAM** (Identity & Access Management) – creates roles & decides who has
access to what. You can create role which have access to all or specific
S3 bucket.

<img src="media/image10.png" style="width:3.13in;height:2.25in" />

<u>Getting Role & Region-</u>

<img src="media/image11.png" style="width:6.26806in;height:1.44375in" />

**CodeBuild** (CI) allows us to build a dedicated Docker image
(environment that contains all of the necessary packages) for each step
of the pipeline e.g. Train, Valuate, Deploy.

**CodePipeline** (CD) the bigger picture. Defines/build the actual
pipeline. The pipeline can be triggered based on some instance(depending
on how frequently you want the pipeline to run). CodePipeline also
offers connectors to most source control services to pull latest
codebase.

<img src="media/image12.jpeg"
style="width:6.26806in;height:5.42222in" />

**<u>How to Launch SageMaker?</u>**

Login to AWS & go to services from top menu.

<img src="media/image13.png" style="width:6.26806in;height:3.52569in" />

<img src="media/image14.png" style="width:6.26806in;height:3.52569in" />

**<u>Using inbuilt XGBOOST model in SageMaker-</u>**

<img src="media/image15.png" style="width:4.29in;height:2.54in" />

Setting the hyper parameters-

<img src="media/image16.png" style="width:2.22in;height:1.25in" />

Format the csv dataset into acceptable to SageMaker and fit to model-

<img src="media/image17.png" style="width:5.06in;height:1.12in" />

<img src="media/image18.png" style="width:5.14in;height:0.25in" />

To view debugger training reports-

<img src="media/image19.png" style="width:6.26806in;height:0.99722in" />

Download the training & profiling reports to current workspace-

<img src="media/image20.png" style="width:6.26806in;height:0.88056in" />

To get XGBOOST training report path-

<img src="media/image21.png" style="width:6.26806in;height:0.70139in" />

To get the link of profile report file-

<img src="media/image22.png" style="width:6.26806in;height:0.98681in" />

Deploying the model-

Path of saved model-

<img src="media/image23.png" style="width:6.26806in;height:0.47569in" />Deploy
by specifying the EC2 instance type-

<img src="media/image24.png" style="width:2.76in;height:0.98in" />

Endpoint name-

<img src="media/image25.png" style="width:2.49in;height:0.42in" />

Evaluate the model from the endpoint created-

<img src="media/image26.png" style="width:5.22in;height:1.8in" />

Confusion Matrix

<img src="media/image27.png" style="width:5.7in;height:2.05in" />

Compute log-loss function for logistic regression

<img src="media/image28.png" style="width:4.69in;height:1.84in" />

<img src="media/image29.png" style="width:4.48in;height:2.83in" />

<img src="media/image30.png" style="width:5.91in;height:0.8in" />

Reference - <https://www.youtube.com/watch?v=6cg5ERPQ2v8>

**AWS Lambda**

AWS Lambda is a serverless compute service.

<img src="media/image31.png" style="width:6.26806in;height:1.49653in" />
