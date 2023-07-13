# GenderDetectionOpenCV


![25cc7a_b3a1bfc552984e71a505729f3d89baed~mv2](https://github.com/ahmetdzdrr/GenderDetectionOpenCV/assets/117534684/21f2ae4a-afc4-40e1-a34a-c08776b5e06e)

We performed gender detection on a CNN architecture using the OpenCV technology.

In this project, we attempted to perform gender detection using the Celeba dataset and OpenCV. For this project, we utilized the InceptionV3 model as a Keras application.
You can visit the website to download the relevant dataset;
http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html

Our dataset consists of over 200,000 images. There is also a separate dataset that contains various attribute classes related to these images. The recommended splitting of the dataset is as follows:

Training: 0 - 162,000

Validation: 162,000 - 182,000

Testing: 182,000 - 202,000

In our project, we scaled these numbers as follows:

Training: 20,000 samples

Validation: 4,000 samples

Testing: 4,000 samples

These samples were used in our project.

*****************************************************************************************************************************************

AN EXAMPLE FROM DATASET

An example of the data in the dataset is shown on an image with three different attributes.

Attractive    1

Gender        0

Young         1

Name: 000103.jpg, dtype: int64

![download](https://github.com/ahmetdzdrr/GenderDetectionOpenCV/assets/117534684/f41c2677-1562-43e4-ba52-73bc4b427c3f)

*****************************************************************************************************************************************

GENDER ANALYSIS

The gender distribution in the dataset has been visualized and analyzed. In the analysis, it is observed that there is no imbalance in the structure.

![download](https://github.com/ahmetdzdrr/GenderDetectionOpenCV/assets/117534684/b517d75a-512e-4b59-af61-527e4cb2ccda)

*****************************************************************************************************************************************

DATA AUGMENTATION

Data augmentation, also known as data augmentation or data amplification, is a technique that involves performing various transformations and manipulations on existing data to increase the size and diversity of the dataset by generating new data samples.
Data augmentation can enhance the performance of machine learning and deep learning models. It can help address class imbalances in the dataset, reduce overfitting, and improve the model's generalization ability. It involves transforming existing data samples from different angles, sizes, rotations, shifts, crops, or color variations to obtain additional data examples.
For example, in image datasets, data augmentation techniques may include horizontal and vertical flipping, rotation, scaling, random cropping, brightness and contrast adjustments, among others.
Data augmentation helps in creating a more diverse and generalized dataset, enabling the model to better generalize and preventing overfitting.

![download](https://github.com/ahmetdzdrr/GenderDetectionOpenCV/assets/117534684/b7c9b8eb-97cf-412c-931f-f20cc7d2a6b1)

*****************************************************************************************************************************************

INCEPTION V3 MODEL STRUCTURE

This is the structure of the Inception-V3 model, developed over the imagenet dataset.
To use the weights in the Inception V3 model, you need to download the weight file from the designated folder and specify the directory path. To download, you can click on the following link:

https://www.kaggle.com/datasets/madmaxliu/inceptionv3/download?datasetVersionNumber=1

Example: InceptionV3(weights='C:\Users\user\inception_v3_weights_tf_dim_ordering_tf_kernels_notop.h5, 
                      include_top=False, input_shape = (img_height, img_width, 3))
                      
![kdXUzu1](https://github.com/ahmetdzdrr/GenderDetectionOpenCV/assets/117534684/c9fa47db-3669-4133-8308-2ce73f69cb52)

*****************************************************************************************************************************************

TRAINING MODEL DIAGRAM

![rWF7bRY](https://github.com/ahmetdzdrr/GenderDetectionOpenCV/assets/117534684/48f03f67-8020-404b-a12a-b5ea56ed640d)

GlobalAveragePooling2D()(x): This line applies global average pooling to the x tensor. Global average pooling reduces the spatial dimensions of the tensor while retaining the channel information.

Dense(1024, activation='relu')(x): This line adds a fully connected dense layer with 1024 units and applies the ReLU activation function to the x tensor.

Dropout(0.5)(x): This line adds a dropout layer with a rate of 0.4 to the x tensor. Dropout randomly sets a fraction of input units to 0 during training, which helps prevent overfitting.

Dense(512, activation='relu')(x): This line adds another fully connected dense layer with 512 units and applies the ReLU activation function to the x tensor.

Dense(2, activation='softmax')(x): This line adds the final dense layer with 2 units, representing the number of classes in the binary classification task. The softmax activation function is used to obtain the probability distribution over the classes.

*****************************************************************************************************************************************

TEST RESULTS

![Ekran görüntüsü 2023-07-14 002358](https://github.com/ahmetdzdrr/GenderDetectionOpenCV/assets/117534684/0a5a36d9-5f8e-4846-a53e-102188f68e5d)

![Ekran görüntüsü 2023-07-14 002348](https://github.com/ahmetdzdrr/GenderDetectionOpenCV/assets/117534684/1cfe0e8c-6b4d-4ac1-9329-c92fd2bc8a0a)

![Ekran görüntüsü 2023-07-14 002352](https://github.com/ahmetdzdrr/GenderDetectionOpenCV/assets/117534684/81a14d8f-93e4-4399-a0a4-2395ef7ea4c1)




