# NLP_20newsgroup

NLP project, currently in progress.

The aim is to understand the textual data as well be able to classify the new categories.

The data set is the 20newsgroup that can be found on this link: [Kaggle 20neswgroup](https://www.kaggle.com/datasets/crawford/20-newsgroups?resource=download)

## text_analysis.ipynb 

This notebook has 3 steps:
- Data preparation
  - Importing data
  - Cleaning data
  - Validation split
  - Tokenazing and padding

- Modeling
  - Baseline model - Logistic Regression
  - Deep learning I - CNN
  - Deep learning II - RNN
  - RoBERTa (work in progress)

- Model comparison (Work in progress)

Each part has an explanation inside the notebook, being some moments where there is no explanation because they are common steps in the data analysis process (like importing).

### Data preparation

This first moment is about importing the data (in this case the 20-newsgroup dataset), however, because it is a small project and lack of computing power, the number of categories was reduced to only 10 instead of using all 20.

Therefore, common operations were performed such as splitting the dataset into training, validation and testing. 

Also, cleaning operations on text data so it can be transformed into a way that the neural network 'can read' (transform text into number, tokenize and create the list of tokens with padding)

### Modeling

After preparing the dataset for modeling, the first step would be to test how a basic algorithm performs with this data.

To do this I implemented a logistic regression, to then get a sense of the minimum expected metrics (looking mainly at training and validation accuracy).

Having the basic metrics, I implemented the first deep learning algorithm, a convolutional neural network (CNN), because, besides being commonly used with images, its structure allows it to be used to find patterns in texts as well.

Remember that for the deep learning algorithms a tuning of hyperparameters was done, within the computational limitations, the best models were saved in
 [Saved models](./saved_models/)

After CNN, I also did the same process for recurrent neural networks (RNN), which are most commonly used for text data. 

In the future, the RoBERTa algorithm will also be implemented, but unlike the ones implemented so far, I expect this one to make use of transfer learning, instead of training from scratch, I will train only the final layers.

## Next steps

- [ ] Add roberta algorithms
- [ ] Make the models comparison section
- [ ] Create an exclusive notebook for the analysis of this dataset
- [ ] (Future) Implement a model to write news of some category from this dataset



