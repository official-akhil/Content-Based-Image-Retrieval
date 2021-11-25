# IR_Project_CBIR

Requirements : 
The Code was run on Virtual Machine with 52 GB RAM which is NVIDIA GPU enabled which helped us to Trained VGG16, ResNet50 and Inceptionv3.
Repository Structure :
The ‘Notebook’ Directory Contains 3 .ipny files (Jupyter Notebook) Here we will see How to run the code. 
The  ‘Sample Retrieval’ Directory Contains 3 Folder [CBIR, Oxford, Paris] which contains Good Retrieval Images from Best Model on 5 Test Images from each Dataset.
How to Run the Code : 
Use latest Version python == 3.9.5 ,GPU must be enabled in order to Perform Tuning using Transfer Learning .
To run the Code : Make sure to load all the Libraries, numpy, pandas, matplotlib, tensorflow.
We will show how to run our code on CBIR Dataset.
1. Download the Dataset.
2. Make sure you are in Dataset Directory and run the Cell in order to generate ‘class-mappings’ dictionary.
 
3. Perform Data cleaning if Necessary then Run the Further Cell to Generate X.npy and y.npy.
 
4.  Perform train-test-split and Generate Train and Test Data.
 
5. Import Pretrained Model [VGG16, ResNet50, Inceptionv3 ] from Keras.applications, Initialize it with ImageNet weights.
 
6. Set Last Layers for the Model by Layers.trainable to ‘true’.
 
7.  Train the model for 50/100 epochs for Hyperparameter Tuning
 
8. Save the Model
9. Extract Feature for every image By removing the Last layer of Model, Save those Features.
10.  Make ‘temp’ dictionary which contains Mapping of Image_path to Label.
 
11. Perform PCA Dimensionality Reduction on Extracted Features.
12. Save the PCA Features in Database.
 
13. Now Take random Test image from ‘temp’ and Run the ‘def evaluation():’ function.
 
14. Hurray!! You got a great Image Retrieval.
