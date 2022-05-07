# octImageClassificationComparison
This is the associated code base for our paper titled, "Comparing Performance of CNN and ViT Models in Retinal OCT Image Classification Task" as part of our final project for the course BMSC-GA 4493 Deep Learning in Medicine - Spring 2022. 

For this project the Labeled OCT Image database from Kermany et al. 2018 was downloaded from Mendeley Data: (https://data.mendeley.com/datasets/rscbjbr9sj/2).

This project features two models, ResNet-18 + CBAM and HuggingFace Vision Transformer module from PyTorch libraries. Vanilla ResNet-18 is also provided as a baseline for performance comparison. Each model and the train/validation/testset CSV files are located in their respective folder. In order to reproduce these results, please download the data into seperate train (108,309 images) and test folders (1000 images) within the directory and install all included python packages.

Our project was ran GPU using the NYU Greene HPC.
