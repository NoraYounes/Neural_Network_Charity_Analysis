# Neural_Network_Charity_Analysis

##  Overview of the Project
The purpose of this project is to develop a binary classification model that is capable of predicting the success of applicants funded by Alphabet Soup. 

## Results

### Data Preproccessing
- Target: IS_SUCCESSFUL (to determine if the funded money was used effectively)

- Features: 
- - APPLICATION_TYPE
- - AFFILIATION
- - CLASSIFICATION 
- - USE_CASE
- - ORGANIZATION
- - STATUS
- - INCOME_AMT
- - SPECIAL_CONSIDERATIONS
- - ASK_AMT
- - The EIN and NAME 

Features Removed:
- EIN (identification column)
- NAME (identification column)

### Compiling, Training, and Evaluating the Model
The model's target accuracy was 75% or more. 

2 Hidden Layers were created to allow the neurons to train on previous input values and identify complex nonlinear patterns. The first hidden layer has 90 neurons, since its a good rule of thumb to have 2-3 times neurons as the number of inputs, 43. The ReLU activation function was selected for the hidden layers because of its efficiency and ability to train on nonlinear data. The Sigmoid activation function was selected for the output layer because its ideal for binary classification. 

1. Original Neural Network Model:
- Input Features: 43
- Hidden Layer 1: 90 Neurons
- Hidden Layer 2: 45 Neurons
- Activation Functions: ReLU (Hidden Layers) and Sigmoid (Output Layer)

<img width="529" alt="nn_model1" src="https://user-images.githubusercontent.com/78664640/124469610-9325d700-dd68-11eb-8c0b-a15dd97ef1a0.png">

The image above shows that the model was unable to meet the target accuracy performance of 75%. In an attempt to increase the model's accuracy performance, the following methods were used:

#### 2. Optimization Attempt 1: Remove Noisy Variable
- Removed APPLICATION_TYPE_Other column

<img width="517" alt="nn_model2" src="https://user-images.githubusercontent.com/78664640/124469652-9e790280-dd68-11eb-88c3-a3b0d7f13fce.png">

The image above shows an improvement to the accuracy, however it was still unable to meet the target accuracy performance of 75%. 


#### 3. Optimization Attempt 2: Add Neurons to Hidden Layers
- Hidden Layer 1: 120 Neurons
- Hidden Layer 2: 60 Neurons

<img width="507" alt="nn_model3" src="https://user-images.githubusercontent.com/78664640/124469690-aafd5b00-dd68-11eb-8875-e40b118f72e3.png">

The image above shows a decrease to the accuracy and failed to meet the target accuracy performance of 75%. 

#### 4. Optimization Attempt 3: Additional Hidden Layer
- Hidden Layer 1: 90 Neurons
- Hidden Layer 2: 45 Neurons
- Hidden Layer 3: 5 Neurons

<img width="503" alt="nn_model4" src="https://user-images.githubusercontent.com/78664640/124469732-b8b2e080-dd68-11eb-9af2-2cbd10121f6e.png">

The image above shows a decrease to the accuracy and failed to meet the target accuracy performance of 75%. 


#### 5. Optimization Attempt 4: Change Activation Function 
- Activation Function: Sigmoid for all layers

<img width="509" alt="nn_model5" src="https://user-images.githubusercontent.com/78664640/124469776-c6686600-dd68-11eb-84c1-bd55ebc89211.png">

The image above shows a decrease to the accuracy and failed to meet the target accuracy performance of 75%. 


## Summary
The neural network model designed to predict the success of applicants failed to meet the accuracy target of 75%. The first attempt to eliminate noisy variables slightly improved the accuracy from 65% to 68% and loss from 2.43 to 1.23. The final attempt that changed the activation function decreased the model's accuracy performance from 65% to 52%, but the loss improved from 2.43 to 0.69. A recommendation to help improve the model's performance would be to use a support vector machine (SVM) model as it is advantageous for binary classification and it can also be used on nonlinear data.