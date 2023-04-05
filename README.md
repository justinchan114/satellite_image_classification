# satellite_image_classification
Satellite image classification of data from EuroSat (https://github.com/phelber/EuroSAT)

## The data
Sentinel-2 satellite images covering 13 spectral bands and consisting out of 10 classes with in total 27,000 labeled and geo-referenced images. Each image has a size of 64x64x3. The data is available in a form of tensorflow_datasets (tfds).

## Methodology
The data set was clean and well organized, so further processing was required. It seperated into train/val/test set, with 60/20/20% of data.
