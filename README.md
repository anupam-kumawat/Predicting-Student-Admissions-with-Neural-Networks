# Student Admissions Prediction with Neural Networks

This Jupyter notebook demonstrates the use of neural networks to predict student admissions to graduate school at UCLA. The prediction is based on three input variables: GRE scores, GPA scores, and class rank.

## Dataset
The dataset used in this notebook was obtained from [this source](http://www.ats.ucla.edu/). It contains the following columns:

- `admit`: Binary variable indicating admission (1) or rejection (0)
- `gre`: GRE scores (Test)
- `gpa`: GPA scores (Grades)
- `rank`: Class rank (1-4)

## Loading the Data
The data is loaded into a pandas DataFrame using the `read_csv` function from the Pandas library. The first 10 rows of the data are printed to provide an overview of the dataset.

## Plotting the Data
A plot of the data is created to visualize the relationship between GRE scores and GPA scores. The data points are color-coded based on admission status (admitted or rejected). The plot helps in understanding the separability of the data.

## Considering Class Rank
To further analyze the data, four separate plots are created for each class rank (1-4). This allows for a better understanding of how class rank relates to admission status.

## One-Hot Encoding the Rank
The class rank column is one-hot encoded using the `get_dummies` function from the Pandas library. This process creates binary indicator variables for each class rank, which are then concatenated with the original data. The original rank column is dropped from the dataset.

## Scaling the Data
To ensure fair handling of features with different scales, the data is scaled before training the neural network. The GPA scores are divided by 4.0 to normalize them within the range of 0-1, and the GRE scores are divided by 800 to bring them within the same range.

## Splitting the Data
The data is split into training and testing sets for evaluating the performance of the trained model. The testing set comprises 10% of the total data, while the training set contains the remaining 90%.

## Training the Neural Network
A 2-layer neural network is trained using the training data. The network is trained using backpropagation and gradient descent. The training process involves iterating through the data for a specified number of epochs, updating the weights, and monitoring the loss on the training set. The loss is printed at regular intervals to track the progress of the training process.

Note: The specific code implementation for training the neural network is not included in this README file.

---
Please refer to the Jupyter notebook for the complete code implementation and detailed explanations of each step.
