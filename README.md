# octImageClassificationComparison
This is the associated code base for our paper titled, "Comparing Performance of CNN and ViT Models in Retinal OCT Image Classification Task" as part of our final project for the course BMSC-GA 4493 Deep Learning in Medicine - Spring 2022. 

For this project the Labeled OCT Image database from Kermany et al. 2018 was downloaded from Mendeley Data: (https://data.mendeley.com/datasets/rscbjbr9sj/2). Please download this dataset (8GB) and place the root OCT folder in the same directory as the model .ipynb file.

This project features two models, ResNet-18 + CBAM and HuggingFace Vision Transformer module from PyTorch libraries. Vanilla ResNet-18 is also provided as a baseline for performance comparison. Each model and the train/validation/testset CSV files are located in their respective folder. In order to reproduce these results, please download the data into seperate train (108,309 images) and test folders (1000 images) within the directory and install all included python packages.

Our project was ran GPU using the NYU Greene HPC.

Notes on creating label CSV files from original data download for use with ResNet models:
The original data was downloaded as 1 directory with  2 sub-directories 'Test, Train' each with 4 folders for each class: 'NORMAL, DRUSEN, CNV, DME'
No label csv files was provided, so label indication was through the image names (example: 'CNV-1112835-371.jpeg').

To work with this data, first we generated train and test csv files from the data directory structure and named them OCT_TrainLabels, OCT_TestLabels.

Then the image data was combined into 1 directory with 2 subfolders: train and test called 'inputOCT'.

inputOCT, OCT_TrainLabels.csv, and OCT_TestLabels.csv were uploaded to HPC for model training.

Trainning and Validation Split:
Inside HPC, OCT_TrainLabels.csv was split randomly into Train_dataset_NEW.csv and Val_dataset_NEW.csv using an 80/20 split.

For hyperparameter tunning, subsets (0.25 of full dataset) were generated, called Train_Subset.csv and Val_Subset.csv

For the ViT model, the ImageFolder class from torchvision was used to gather images and class labels from the respective folders the images are contained in. Datasets were created from 
