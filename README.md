# Deep Learning on KMNIST (Kuzushiji-MNIST) Dataset
- CM3015 Machine Learning and Neural Networks
- End-term Coursework Report

This repository contains the final assignment and project for Goldsmiths, University of London module CM3015.

## Introduction
For this project, the dataset used to undergo deep learning is known as Kuzushiji-MNIST (or KMNIST) from TensorFlow datasets. This dataset is utilized because it has a large-enough dataset for training and testing, with a total of 70,000 grayscale images. This dataset is also a drop-in replacement for the MNIST dataset.

KMNIST is a dataset consisting of Kuzushiji characters, which refers to ancient cursive Japanese characters or scripts in old Japanese texts and manuscripts. The cursive nature of the characters makes the deep learning and classification of the characters difficult, as there are multiple variations for every character. This means that the model to be developed for this classification problem have to be more robust than that of the MNIST dataset. With only 70,000 images, the dataset may not contain every Kuzushiji character and may reflect certain inaccuracies if comparing the results against a different Kuzushiji dataset.

## Goal
This project aims to use deep learning to classify and predict Kuzushiji characters with the use of Kuzushiji-MNIST (KMNIST) dataset. This is achieved by developing a sufficiently robust neural network model that can accurately classify Kuzushiji characters with high accuracy, f1-score and cohen's kappa score.

**Accuracy** represents the number of correct classifications over the total number of classification attempts, and the goal is to achieve >80% accuracy. <br>
**F1-Score** indicates the overall performance of the classification model and can reflect on how it can correctly identify positive cases while minimizing false positives and negatives. The goal is to achieve >80% f1-score. <br>
**Cohen's Kappa Score** indicates the classification model's accuracy, and the goal is to achieve >80% score. <br>

## Approach
- Conduct data split on the dataset.
- Reshape & tranform the data to prepare for deep learning models.
- Develop underfitting and overfitting models.
- Develop regularized models on either of the previous models.
- Use appropriate regularized model on entire dataset, and evalute the results.

## Results and Evaluation
To summarize the findings when developing the appropriate model, I have collated them below. It is important to note that solely using accuracy and loss as the primary metric can miss out on key details such as underfitting or overfitting of the model. The 'combined regularized model' performed the best without underfitting or overfitting. >

1. Underfitted Model
  - Accuracy: 80%
  - Loss: 65% <br>
2. Overfitted Model
  - Accuracy: 95%
  - Loss: 30-35% <br>
3. Dropout Regularized Model
  - Accuracy: 95%
  - Loss: 20%
4. L1/L2 Regularized Model
  - Accuracy: 90%
  - Loss: 45%
5. Combined Regularized Model
  - Accuracy: 95%
  - Loss: 30%
6. Final Model
  - Accuracy: 88%
  - Loss: 68%

Finalized model is based on the 'combined regularized model' with the result of around 88% accuracy, f1-score, and cohen kappa's score. All these metrics have exceeded the goal stated above of having at least 80%. This means that the classification deep learning model developed for the KMNIST dataset meets the goals and does well in classifying the images. It is also important to state that the loss for this model is high, and the development method for the final model may not be optimal. The high loss value could be caused by many different factors and is difficult to evaluate on its own. Further development along with use of other methods and models can bring a more comprehensive evaluation to this project.

## Conclusion
I have developed a model that performs well with the KMNIST dataset by utilizing the hold-out validation method. The model uses the overfitted model as the base before regularizing it with both dropout and L1 and L2 regularization. As mentioned in the results and evaluation section, the final model meets the goals and produces accurate results in classifying the KMNIST images correctly.

While the results of the final model shows it performing well with the KMNIST dataset, other methods and techniques can be employed and may perform better. Further developments and testing with other techniques such as cross-validation or k-folds iteration could produce better results than the hold-out validation method. The use of other techniques in during the regularization of the models could also produce better results.
