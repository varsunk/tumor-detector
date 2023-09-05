# Tumor Detector
This project was one I pursued as a means of understanding and working with CNNs while also attempting to create something that has a tangible impact (tumor detection). This is a continuation of a 3rd place hackathon project that I worked on in the past but aims to be both more useful and more accurate than our old model.

In particular, the dataset for this project is hugely improved over the old project, with over 7000 images in total compared to the less than 1000 images in our original model. Furthermore, I switched the architecture used from a pretrained VGG16 model to a fresh Resnet18 mode, which yielded faster training times and better accuracy over a larger dataset. The dataset also includes four different classes (three of which are distinct tumor types and one of which is a "no tumor" class) as opposed to the more simple scheme used in our original project ("no tumor" or "tumor"), which makes our model much more practical in determining the specific type of tumor as opposed to just identifying whether or not a tumor is present.

# Usage
In order to train the model that I've included in cnn.ipynb, you simply need to download the dataset from [this](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset) Kaggle page.

After this, place the zip file in the same directory as cnn.ipynb and run all of the cells in the notebook. This will unzip the dataset, store it in a new directory called 'dataset', and train the model for 30 epochs. 

# Results
Depending on your compute power, training this model can take between a few minutes and a few hours. On my computer (Intel i5-7400 and a GeForce GTX 1060 6gb), training the model took just over 11 minutes. If you are having memory issues, try lowering the batch size until the model is able to train multiple epochs in succession.

By the end of training, I found that my model, which uses PyTorch's implementation of Resnet18, had reached 100% accuracy on the training data and 98.4% accuracy on the test data.

![Image showing Train and Test accuracy of the model](image.png)

# Tech Used
This project was implemented using mainly PyTorch.

# Credit
The dataset for the project was downloaded [here](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset).