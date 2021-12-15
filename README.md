# Moderating and Classifying Documents using Amazon Rekognition and Amazon Textract

## Summary
This scalable, secure and automated solution allows users to moderate, classifyand process documents using Amazon Rekognition, Custom Labels and Amazon Textract. It allows faster document processing, higher accuracy and reducing the complexity of data extraction. It also provides better security and compliance with personal data legislation by reducing the human workforce involved in processing incoming document.

## Training Pipeline
In the training pipeline, we will label the documents using Amazon SageMaker GroundTruth. We then will use the labeled documents to train a model with Amazon Rekognition Custom Labels.

![](TrainingPipeline.png)

### Installation
Region| Launch
------|-----
US East (N. Virginia) | [![Launch in us-east-1](docs/images/launch-stack.png)](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/new?stackName=doc-moderation-classification-training-pipeline&templateURL=https://aws-rek-immersionday-us-east-1.s3.amazonaws.com/TrainingPipeline.yaml)
US West (Oregon) | [![Launch in us-west-2](docs/images/launch-stack.png)](https://console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/new?stackName=doc-moderation-classification-training-pipeline&templateURL=https://aws-rek-immersionday-us-east-1.s3.amazonaws.com/TrainingPipeline.yaml)

## Inference Pipeline

In the inference pipeline, we will:
1. Perform moderation on uploaded documents using Amazon Rekognition.
2. Classify documents into different categories such as W-2s, invoices, bank statements, pay stubs using Amazon Rekognition Custom Labels.
3. Store meta-data (moderation and classification labels) in to Amazon DynamoDB table.
4. Extract text from documents such as printed text, handwriting, forms, and tables using Amazon Textract.

![](InferencePipeline.png)

### Installation
Region| Launch
------|-----
US East (N. Virginia) | [![Launch in us-east-1](docs/images/launch-stack.png)](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/new?stackName=doc-moderation-classification-inference-pipeline&templateURL=https://aws-rek-immersionday-us-east-1.s3.amazonaws.com/InferencePipeline.yml)
US West (Oregon) | [![Launch in us-west-2](docs/images/launch-stack.png)](https://console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/new?stackName=doc-moderation-classification-inference-pipeline&templateURL=https://aws-rek-immersionday-us-east-1.s3.amazonaws.com/InferencePipeline.yml)

# Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

# License

This library is licensed under the MIT-0 License. See the LICENSE file.
