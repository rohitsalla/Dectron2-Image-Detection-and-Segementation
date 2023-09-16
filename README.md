# Detection and Segmentation
 ## Detection and segmentation using detecton2

 # steps to build detectron2
1) Right now it only support ubuntu and MacOS.
2) Installation:
  i) Using pip 
    python -m pip install 'git+https://github.com/facebookresearch/detectron2.git'
  ii) Using clone
    git clone https://github.com/facebookresearch/detectron2.git
    python -m pip install -e detectron2
  iii) If you have cuda(GPU) :
    There are different wheel links for each torch and cuda :
    Please refer below link for same.
    https://detectron2.readthedocs.io/en/latest/tutorials/install.html#install-pre-built-detectron2-linux-only



## Steps needed to build the environment
  ### pip3 install -r requirements.txt


## Video indexes
    1. Buisness use Case and Understanding of data . 
    2. Difference between classification,detection and Segmentation .
    3. State of Art - Detection and Segmentation
    4. Building/Installing Detectron 
    5. Understanding detectron2 from docs-Basics
    6. Running detectron2 using built-in datasets .
    7. Starts setting up Detectron2 - Training -Part 1
    8. Starts setting up Detectron2 - Training -Part 2
    9. Augmentation Techniques for Detectron
    10. Inference script and how to  test on test image
    11. Understanding how to interpret results from Detectron2
    12. Understanding visulaize.py for visualizing results
    13. Plot detection and segmentaion separately .
    14. Understanding  Project Structure for Training and training .
    15. Understanding  Project Structure for Inference and Infer .

Objective 
Antibiograms are often used by clinicians to assess local susceptibility rates to select 
empiric antibiotic therapy, and monitor resistance trends over time. The testing occurs 
in a medical laboratory and uses culture methods that expose bacteria to antibiotics 
to test if bacteria have genes that confer resistance. Culture methods often involve 
measuring the diameter of areas without bacterial growth, called zones of inhibition. 
The zone of inhibition is a circular area around the antibiotic spot in which the bacteria 
colonies do not grow. The zone of inhibition can be used to measure the susceptibility 
of the bacteria to the antibiotic. The process of locating the zones and related 
inhibitions can be automated using image detection and segmentation.
Image Classification helps us classify what is contained in an image, whereas object 
Detection specifies the location of multiple objects in the image. On the other hand, 
image Segmentation will create a pixel-wise mask of each object in the images, which 
helps identify the shapes of different objects in the image.
We have dealt with image classification in the project, Build a Multi Class Image 
Classification Model Python using CNN. This project will perform image detection and 
segmentation on a given set of images to detect the zones and inhibition of the bacteria 
present in a collection of images using the Detectron2 model.
Data Description
The dataset contains several antibiogram test images divided into training and testing 
folders. There are around 50 images in the training dataset and five in the testing.

Tech stack 
 Language - Python
 Libraries - torch, detectron2, cv2, matplotlib, numpy
Approach 
1. Import Detectron2 using the git command
2. Importing the required libraries.
3. Setup the input, output, train, test and annotations.json path
4. Register the coco instances with register name and annotations and form a
dataset with configurations (in metadatacatalog)
5. Data Visualization
6. Training the Dectectron2 model
 Define a class for coco Trainer
 Get the default configurations from cfg and add the necessary 
parameters 
 Load the pre-trained model weights.
 Perform training on the data.
7. Inference model
 Set the default config file and add the required parameters
 Define an inference image
 Load the weights of trained model
 Define default predictor object
 Make the predictions and visualize the results.
 Interpret the generated results
 Plot the bounding boxes and masks in a given image
Modular code overview
Description
Once you unzip the modular_code.zip file, you can find the following folders within it.
1. Input
2. Source Folder
3. Output
4. Lib
1. Input folder - It contains all the data that we have for analysis. We have two 
folders. Training_data and testing_data. The following three subfolders are 
present
 driving_license
 social_security
 others
2. Source folder - This is the most important folder of the project. This folder 
contains all the modularized code for all the above steps in a modularized 
manner. This folder consists of:
 Engine.py
 ML_Pipeline
The ML_Pipeline is a folder that contains all the functions put into different 
python files, which are appropriately named. These python functions are 
then called inside the engine.py file.
3. Output folder - The output folder contains the fitted model that we trained for this 
data. This model can be easily loaded and used for future use, and the user 
need not have to train all the models from the beginning.
4. Lib - This folder contains two notebooks. 
 training_classification.ipynb
 Inference.ipynb
There is a ppt present in the reference subfolder. This is the one used during 
the presentation.
