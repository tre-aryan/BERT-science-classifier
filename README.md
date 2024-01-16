# BERT-science-classifier
## Aryan Trehan | atrehan@usc.edu

Using Fine-Tuned BERT for Science text Physics/Chemistry/Biology Classification on reddit text data

## Dataset

"Physics vs Chemistry vs Biology" accessed on https://www.kaggle.com/datasets/vivmankar/physics-vs-chemistry-vs-biology/data

Number of classes: 3 (Physics, Chemistry, and Biology)

Total number of data points: 10281 comments

The number of words in train comments ranges from 1 word to 1274 words

The number of words in test comments ranges from 26 words to 837 words

## Model Development and Training

Since the task in question is one of text classification an encoder network like BERT would be most suitable for the resources available. 

After testing multiple hugginface models, I settled on 'bert-base-uncased' as it had the most efficient results with acceptable training times on the Google Colab T5 GPU.

## Model Evaluation/Results

The main metric for evaluation chosen is model accuracy after epochs.

Below is the trend in validation accuracy and loss per epoch

Epoch 1, Average Loss: 0.4360759374137749
Validation Accuracy: 0.8291298865069356

Epoch 2, Average Loss: 0.31252703408245
Validation Accuracy: 0.8530895334174022

Epoch 3, Average Loss: 0.23269713845665513
Validation Accuracy: 0.8562421185372006

In the end the model performed quite well

## Discussion

How well does your dataset, model architecture, training procedures, and chosen metrics fit the task at hand? 
- My goal with this project was to explore and understand the pipeline for finetuning encoder models for classification tasks. The dataset chosen is a great way to test the efficacy of my training procedure. The choice of bert-base was apt due to the prior work that showcased its ability in encoder based tasks. Finally, accuracy and average loss are good metrics to observe the performance of the model especially since large language models take a long time to train and evaluate.

Can your efforts be extended to wider implications, or contribute to social good? Are there any limitations in your methods that should be considered before doing so?
- Even though the current dataset that the model has been applied to appears to be disconnected from social good, the pipeline developed can be used for many text classification tasks that significantly impact society. Text classification can be applied to social media posts to aid in disaster response or to academic literature to aid in research and drug discovery.

If you were to continue this project, what would be your next steps?
- Figuring out how to parse and process inputs greater than the 512 token limit that BERT has!! I had to scrap an entire earlier project because my inputs were large chunks of text that carried meaningful information for classifcation throughout the body. Truncation was causing a significant drop in accuracy. Therefore, I would hope to explore methods like moving window and summarization to process larger pieces of text with BERT based encoders. 

