# Butterfly Identification
Butterfly Identification models for the contest : https://aiplanet.com/challenges/325/butterfly_identification/overview/about

### Models Observations
1. DenseNet121- Trained for 20 epochs; 95.06% training accuracy 
1. VGG16- Trained for 10 epochs; 56.88% training accuracy 
1. ResNet50- Trained for 38 epochs; 27.13% training accuracy 

### Dataset
Link : https://s3.us-west-1.wasabisys.com/dphi/public-datasets/Data_Sprint_107_Butterfly_Classification/butterflies.zip

The dataset features 75 different classes of Butterflies. The dataset contains about 1000+ labelled images including the validation images. Each image belongs to only one butterfly category and are saved in separate folders of the labelled classes

### Data Preprocessing
1. Images in 'Train' subfolder was separated into respective subfolders based on the butterfly class using label feature from 'Training_set.csv'.
2. A validation set was created by sampling 5 images from each butterfly class.
3. Images rescaled to the range of 0 to 1 (each pixel value was divided by 255).

### Model Training
1. Train image values were re-scaled to the range of 0 to 1 (each pixel value was divided by 255).
2. Models from tf.keras.applications such as DenseNet121, VGG16 and ResNet50 were used with include_top = False to provide custom classification layer, weights = 'imagenet' to get weights of model that was trained on a image database instead of starting with random weights, an average pooling layer and the output layer with 75 classes.
3. Model was fed input images in batches of 32 using ImageDataGenerator 'flow_from_directory'.
 
### Possible Improvements
1. Fix class imbalance.
2. Test on more models; Train VGG16 for more epochs.
3. Decrease the image dimension.
4. Test set accuracy.
