## Moderating and Classifying Documents using Amazon Rekognition and Amazon Textract

### Summary
This scalable, secure and automated solution allows users to moderate, classifyand process documents using Amazon Rekognition, Custom Labels and Amazon Textract. It allows faster document processing, higher accuracy and reducing the complexity of data extraction. It also provides better security and compliance with personal data legislation by reducing the human workforce involved in processing incoming document.

### Training Pipeline
In the training pipeline, we will label the documents using Amazon SageMaker GroundTruth. We then will use the labeled documents to train a model with Amazon Rekognition Custom Labels.

![](TrainingPipeline.png)

### Inference Pipeline

In the inference pipeline, we will:
1. Perform moderation on uploaded documents using Amazon Rekognition.
2. Classify documents into different categories such as W-2s, invoices, bank statements, pay stubs using Amazon Rekognition Custom Labels.
3. Extract text from documents such as printed text, handwriting, forms, and tables using Amazon Textract.

![](InferencePipeline.png)

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.