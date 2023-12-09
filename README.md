# Comp432-GroupP: 
This is a machine learning project for the Concordia class COMP-432.<br>
The project consists of training and using pre-trained machine learning models in order to solve a classification problem. <br>
### Datasets used in the project: 
For this project, three different datasets are used. Two of them are related to cancer classification, while the third one is used for animals classification. The datasets are obtained from two popular sites commonly used for machine learning: [Kaggle.com](https://www.kaggle.com) & [Zenodo.org](https://zenodo.org) <br>
The Datasets were simply downloaded using the provided links and integrated in our code with the help of file handling libraries such as pyTorch.
##### Dataset 1 (Colorectal Cancer Classification): [[Original Dataset](https://zenodo.org/records/1214456) | [Project Dataset](https://onedrive.live.com/?authkey=%21ADmb8ZdEzwFMZoo&id=FB338EA7CF297329%21405133&cid=FB338EA7CF297329&parId=root&parQt=sharedby&parCid=UnAuth&o=OneUp)]<br>
This is a dataset of 100k image patches split into 8 different classes identifying the tissue type, including Adipose (ADI), background (BACK), debris (DEB), lymphocytes (LYM), mucus (MUC), smooth muscle (MUS), normal colon mucosa (NORM), cancer-associated stroma (STR), and colorectal adenocarcinoma epithelium (TUM). In this project, we will be using a reduced version of the dataset, containing 6K image patches split into 3 classes: smooth muscle (MUS), normal colon mucosa (NORM), and cancer-associated stroma (STR).<br>
##### Dataset 2 (Prostate Cancer Classification): [[Original Dataset](https://zenodo.org/records/4789576) | [Project Dataset](https://onedrive.live.com/?authkey=%21APy4wecXgMnQ7Kw&id=FB338EA7CF297329%21405132&cid=FB338EA7CF297329&parId=root&parQt=sharedby&parCid=UnAuth&o=OneUp)]<br>
This is a dataset of 120k image patches split into 3 different classes identifying the tissue type, including Prostate Cancer Tumor Tissue, Benign Glandular Prostate Tissue, and Benign Non-Glandular Prostate Tissue. For this project, the dataset is reduced to 6k image patches for the same 3 classes. <br>
##### Dataset 3 (Animal Faces Classification): [[Original Dataset](https://www.kaggle.com/datasets/andrewmvd/animal-faces) | [Project Dataset](https://onedrive.live.com/?authkey=%21AKqEWb1GDjWPbG0&id=FB338EA7CF297329%21405131&cid=FB338EA7CF297329&parId=root&parQt=sharedby&parCid=UnAuth&o=OneUp)]<br>
This is a dataset of 16k images split into 3 different classes identifying animal types, including Cats, Dogs, and wildlife animals. For this project, the dataset is reduced to 6k images for the same 3 classes.

### Project's main goal:
The goal of the project was to design and train a CNN ResNet-18 encoder on Datset #1 and applying that same model on Dataset #2 & Dataset #3 to analyze the difference in performances. <br><br>
To start, our team researched several common CNN architectures and ended up choosing ResNet-18. We split the first dataset for training and testing, designed and trained the ResNet-18 CNN model on the training set and tested it afterwards on the testing set. <br>
Afterwards, the model was also applied to Dataset #2 and Dataset #3. Next, a different pre-trained CNN encoder from the pytorch library was chosen (ImageNet) and was applied on Dataset #2 & Dataset #3. The CNN model that we built oursleves as well as the pytorch CNN model were then compared in terms of their performances (loss and accuracy). To help with the reporting, different classification reports were produced in addition to plots to help visualize the performance of the models at each training epoch. <br><br>
Finally, the output features of the CNN encoders were analyzed using t-SNE, Logistic Regression and K-nearest neighbour clustering on Dataset #3. 

# Contributors: 
- Arsany Fahmy (40157267) ~Arsollo
- Vyacheslav Medvedenko (40134207) ~Vyacheslavium
- Khalil Azaiez (40201439) ~Khalilazaiez
- Bozhidar Leshev (40105294) ~BozhidarLeshev

# Requirements & Dependecies:
- PyTorch
- OS
- Numpy
- Matplotlib
- Sklearn
- PIL

# How to train/validate our model:
Training the model:
  
  1-Upload the dataset over to Google drive.
  
  2-Open the "Training and testing the ResNet-18 Model.ipynb" file with GoogleColab
  
  3-In the 3rd code block, copy and paste the dataset path (google drive path) over the datset1_path variable:
  
  ![image](https://github.com/Arsollo/COMP432-GroupP/assets/52761503/42e006e7-b9a3-4607-af31-e2db0b096e10)
  
  4-In the 11th code block, copy and past the desired path (google drive path) to save the model and the optimizer, over the save_dir and save_dir_opti variables:
  
  ![image](https://github.com/Arsollo/COMP432-GroupP/assets/52761503/6e235a19-3716-4619-88cb-b3c26fd0891a)
  
  5-In the top right corner of the Google Colab, connect to a T4 GPU server:
  
  ![image](https://github.com/Arsollo/COMP432-GroupP/assets/52761503/8dacec3a-945c-4273-8b41-9bab7c3fc8f2)
  
  6-Run all code blocks in sequence, up to and including code block 11 ("# Training the CNN ResNet-18 Model").
  
  7-It will take 30mins - 60mins to run the training cycle.
 
  8-Run code block 12 if graphs are required.
  

# How to run the pre-trained model on the provided sample test dataset: 
Testing the model:
    
  1-Upload the dataset over to Google drive.
  
  2-Open the "Training and testing the ResNet-18 Model.ipynb" file with GoogleColab
  
  3-In the 3rd code block, copy and paste the dataset path (google drive path) over the datset1_path variable:
  ![image](https://github.com/Arsollo/COMP432-GroupP/assets/52761503/42e006e7-b9a3-4607-af31-e2db0b096e10)
  
  4-In the 13th code block ("#Classification Report on training data"), copy and past the path (google drive path) to the model to load, over the save_dir variable:
 
 ![image](https://github.com/Arsollo/COMP432-GroupP/assets/52761503/c3d734d6-9956-43e9-915a-6dd3dfc6ecc7)


  5-In the 14th code block ("#Testing the model on Dataset #1"), copy and past the path (google drive path) to the model to load, over the save_dir variable:
  
  ![image](https://github.com/Arsollo/COMP432-GroupP/assets/52761503/28ae3509-385a-4a9c-96cd-9ef7b8e8be84)

  6-In the top right corner of the Google Colab, connect to a T4 GPU server:
  
  ![image](https://github.com/Arsollo/COMP432-GroupP/assets/52761503/8dacec3a-945c-4273-8b41-9bab7c3fc8f2)
  
  7-Run all code blocks in sequence, excepth code block 11 and 12.
    
  Code block 13 ("#Classification Report on training data") will run the model, in prediction mode, over the TRAINING DATA and print the classification report.
    
  Code block 14 ("#Testing the model on Dataset #1") will run the model, in prediction mode, over the TESTING DATA and print confusion matrix and the classification report.
    
  8-It will take 30mins - 60mins to run the testing cycle.



# Colab Main Files:
The majority of the coding was implemneted on two seperate Colab files. <br>
In the first file, we uploaded the three datasets, preprocessed them and visualized them and we also designed, trained and tested the ResNet-18 model on Dataset #1 <br>

#### [Training and testing the ResNet-18 Model on Dataset#1.ipynb](https://colab.research.google.com/drive/19xycOefX7l8RE1pfRWApMzE0WxNqjuG6)

In the second file, we applied t-SNE on the 4 different scenarios and we also applied Logistic Regression and K-nearest neighbour clustering on Dataset #3.

#### [t-SNE Feature extraction for 4 scenarios & LR and KNN on Dataset #3](https://colab.research.google.com/drive/1bMYTCn0ksrIRmdwLOQLc7KklEnJYAg3i#scrollTo=cRHgX_4OxyTW)

# Video Presentation:
To present our work, a short 8 minutes presentation video was produced: 




  
