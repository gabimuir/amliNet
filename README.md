# amliNet
Automated Medical Lung Imaging Net:
Using machine learning to predict pathologies from chest x-rays.

The amliNet team: Alex, Vita, Gabi

## The Dataset
The data we used to train and test our models is the CheXpert dataset, created by researchers at Stanford. The data is avaible after filling out the form on the bottom of their website: https://stanfordmlgroup.github.io/competitions/chexpert/ Our models all used the downsampled resolution images, called the 'small' set. 

## Using the data
A few methods were attempted to wrangle the data. The downloaded data came in a 12gb zip file. We created a method to edit the path of the images so no matter where the model is being run (jupyter in a separate folder, google colab, the cloud), the images are accessable.
### Method 1: Unzipped locally, models run locally with Jupyter notebook
Download the zip file and unzip onto the hard drive (unzipped size also approximately 12 gb). Run a jupyter notebook and make sure to edit the PATH variable to the location of the unzipped dataset directory.

### Method 2: Uploaded to Google Drive as zip file, unzipped each day in Google Colab
The zipped file fits great on Google Drive, but Google Drive is unable to handle the number of subdirectories within the training data, and will always fail to unzip. Luckily, Google Colab exists and works very similarly to Jupyter notebook, with easy access to Google Drive. Colab can unzip the file to the runtime, which will persist on that runtime for a whole day. The data can then be used like it was on a local hard drive.

### Method 3: Upload to Google Cloud Bucket, run models on Google Cloud virtual machine
We uploaded the unzipped file to a google cloud bucket, then launched an instance of the google cloud virtual machine and edited Jupyter notebooks through there. The results were very slow, so Google Colab was the option we mostly chose to use.

## Our models
We have run a number of different models: DenseNet121, ResNet, Simple CNNs, and more. We have also provided a template where any number of models can be tested or custom created. 

