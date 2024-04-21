
# Age and Gender Classification via Neural Nets and Transfer Learning

While deep neural networks have yielded high accuracies in classifying age and gender, creating them from scratch can be very computationally expensive. Furthermore, the datasets accessible to the public lack a sufficient amount of labeled data for both age and gender, which poses a challenge in effectively training a deep neural network to achieve optimal performance. Hence, this paper introduces a model that leverages on transfer learning, whereby a pre-trained face recognition model is reused and adapted for age and gender classification.

<br>

In this study, we utilized the VGG16 architecture as our core model. VGG16 is a 16 layer deep network widely popular for its high accuracy in many computer vision tasks. It consists of 13 ReLU activated convolutional blocks for feature extraction, 4 max pooling layers in between and three dense layers for classification (Figure 1).

<img width="939" alt="Screenshot of App" src="/static/vgg16.png">

Figure 1

<br>

By employing transfer learning, the training of VGG16 for age and gender classification becomes significantly more efficient.

<br>

<img width="939" alt="Screenshot of App" src="/static/Model.png">

Figure 2

<br>

In our proposed model, all convolutional layers as well as the first dense layer of the VGG16 architecture is pre-trained on a larger general purpose dataset for feature extraction from facial images. Another 3 untrained dense layers are added for the classification of each task, respectively. This approach offers an efficient and effective means of obtaining two labels for each input data, as illustrated in Figure 2.

<br>

Our results how the use of transfer learning can expedite the convergence of the model using well-learned features of facial images allowing it to adapt and specialize in age and gender classification tasks with relatively few training epochs while reducing overfitting. More information can be found in our report.

<img width="939" alt="Screenshot of App" src="/static/Age.png">

<img width="939" alt="Screenshot of App" src="/static/Gender.png">