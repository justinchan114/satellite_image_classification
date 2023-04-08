# satellite_image_classification
Satellite image classification of data from EuroSat (https://github.com/phelber/EuroSAT)

## The data
Sentinel-2 satellite images covering 13 spectral bands and consisting out of 10 classes with in total 27,000 labeled and geo-referenced images. Each image has a size of 64x64x3. The data is available in a form of tensorflow_datasets (tfds).

## Exploratory data analysis 
The data set was visualized and appeared to be clean and well organized, so further processing was not required. It is then seperated into train/val/test set, with 60/20/20% of data.

## Model training
EfficientNetV2B0 was used as base model (which has an input of 64x64x3 and output 2,2,1280), on top of that is a GAP2D layer to flatten the layers to 1D 1280 vector, which was then passed to softmax for 10 class output. It was trained for 5 epochs and has a accuracy of 94% on validation set.

##Results on test set
The model has a macro-weighted f1-score of 0.954. To further improve the performance, we may further introduce cross validation or introduce few more epochs. But as the data set is not small and compulational heavy for google colab, it was not trained with cross validation in this exercise.
