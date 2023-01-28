# Toxicity Text Classification

**Dataset:**

This project uses data from the Civil Comments platform. The platform closed in 2017 and released its comments to the public. Jigsaw, a unit within Google, annotated the data by asking human raters to rate the toxicity of the comments. 

The value of toxicity and its six subtypes severe toxicity, obscene, threat, insult, identity attack, and sexual explicit, ranges between 0 and 1, which respresents the fraction of raters who believe the comment falls under the label. The labels are mutually inclusive.

 More information can be found at: https://www.kaggle.com/competitions/jigsaw-unintended-bias-in-toxicity-classification

<br>

**Project Objectives:**

(1) Jigsaw's competition asked individuals to develop a model to classify whether a comment is toxic. A comment is considered toxic if toxicity >= 0.5. Instead of the binary classification approach, I am going to predict the degree of toxicity or probability of each comment falling under the six subtypes

(2) Demonstrate how to fine-tune state-of-the-art architecture BERT from Hugging Face's Transformer library

<br>

**Results:**

(1) Using KL-Divergence as the evaluation metric, the returned KL-Divergence scores for the toxicity subtypes severe toxicity, obscene, threat, insult, identity attack, and sexual explicit are relatively decent, with a few high scores over 10 for insult, threat, and obsence comments. **The reported scores are based on fine-tuning the BERT model on 700 records and evaluating it against 300 records from the dataset with ~2 million records in total.** This is because BERT is a large NN architecture and Amazon Sagemaker Studio Lab's free GPU provision does not have enough RAM to pre-process and train on more data. Therefore, the KL-Divergence scores would be significantly lower if the model was fine-tuned on more data points

(2) Despite the RAM limitation, I was able to demonstrate how to load and apply the tokenizer and model

<br>

**Opportunities:**

(1) The RAM limitation prevented me from fully showcasing BERT's powerful capabilities. To jump over this hurdle, I would explore and leverage GPU instances from cloud computing platforms 
