# Comparative Analysis of Neural Network Architectures for Brain Tumor MRI Segmentation Using SimpleITK

## ResNet Model Setup

### Steps for Execution:

1. Load the Dataset
   - Upload the 'archive_brain_mri_100.zip' (Drive link: https://drive.google.com/file/d/1RVoLx3aswRNYMvnMaR5tEyxFd36fVkPu/view) file to your environment, either in Google Colab or on your local machine.

2. Execute Notebooks
   - Open and execute the code in the 'Augmented_Brain_MRI_dataset' Jupyter notebook.
   - Afterward, execute the 'Med_Img_Final_Project_v4' Jupyter notebook.
     NOTE: Running this notebook requires access to an NVIDIA T4 GPU as a minimum hardware requirement.

### Required Python Libraries:
- numpy
- torch
- torchvision
- tqdm
- SimpleITK
- matplotlib

### Run
To install the required libraries, run the following command:

pip install numpy torch torchvision tqdm SimpleITK matplotlib

### Additional Notes:
- Ensure that your environment supports GPU acceleration (e.g., Google Colab or a local machine with a compatible GPU).
- Verify that your Python version is compatible (Python 3.6+ recommended).


## nnU-Net Model Setup

This will provide an overview for how to set up and run the nnU-Net model on the BraTS data.


### Files

Make sure to have the following files in your Google Drive (My Drive). We will use them to load into Google Colab

 - BraTS data: https://drive.google.com/file/d/1frWxlGUgwPoe8rKncK8boJiTQoMn8E-A/view?usp=sharing
 - dataset.json (lists data characteristics): https://drive.google.com/file/d/1nupjapuGvognIw09ihoRwXAH6O4j0ysm/view?usp=sharing
 - splits_final.json (data split is randomly generated, but fixed): https://drive.google.com/file/d/1abI7SEao9tTlq5BuYByRgs1YTZ0BzbSY/view?usp=sharing

### Code Structure

'nnunet.ipynb' will walk through the entire process, from downloading initial BraTS data, converting to the desired nnU-Net format, performing augmentations, pre-processing the data, training the model, and saving the results.

Brief explanations are provided above each code block.

### Interpreting the Results

Results can be found in the 'nnUNet_results' and 'nnunet_output' directories.

#### nnUNet_results/

Training results are organized by the data split used, which was '1' within the code. Key contents include:

 - the training log
 - trained models, as '.pth' files
 - training graph, as 'progress.png'

#### nnunet_output/

This directory includes the inference output on training data:
 - The model output for each testing example, as 'BRATS_XYZ.nii.gz
 - A copy of the dataset file, dataset.json
 - A copy of the nnU-Net self configured training files, plans.json
 - The inference parameter file, predict_from_raw_data_args.json

### Results will be saved to your Drive

Please comment out the related sections if local results visualization is not desired.


