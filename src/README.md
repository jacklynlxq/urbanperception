# Pipeline of Data Preprocessing to Visualisation
This describes the pipeline of the whole project.

Data Preprocessing -> Download GSV for Training-> Training -> Download GSV for Prediction -> Prediction -> Visualisation

## Data Preprocessing
1. Download PlacePulse2.0 Dataset(Archived by the MIT Media Lab)
2. Run all cells in `"Data Preprocessing/Data Preprocessing.ipnyb"`
3. Run all cells in `"Data Preprocessing/Remove Duplicates from the Result of Combination of Left and Right Winners.ipynb"`
4. Run all cells in `"Data Preprocessing/Annotations.ipnyb"`

## Download GSV for Training
1. Run all cells in `"Download GSV/Download GSV Images Training.ipynb"`
2. [Optional for Data Augmentation] Run all cells in `"Download GSV/Download GSV Images Angle 90.ipynb"` 
3. [Optional for Data Augmentation] Run all cells in `"Download GSV/Combine Augmented Data.ipynb"`

## Training
Run all cells in `"Training/train.ipynb"`
Note: Transfer Learning was done using the Keras VGG16-places365 pretrained model provided by https://github.com/GKalliatakis/Keras-VGG16-places365

## Download GSV for Prediction 
1. Draw neighbourhood map
2. Run all cells in `"Visualisation/Snap to Roads API.ipynb"`
3. Run cells in `"Download GSV/Download KL GSV Images.ipynb"`

## Visualisation
1. Run all cells in `"Visualisation/Geocoding API.ipynb"`
2. [Done in QGIS] Average perceptual scores for each perceptual attribute for each neighbourhood
3. [Done in QGIS] Draw Choropleth Maps for each perceptual attribute
4. [Done in QGIS] Get predominance attribute for each neighbourhood
5. [Done in QGIS] Get strength of predominance for the predominance attribute

     - Note: Formula for strength of predominance 
     
          <img src="https://render.githubusercontent.com/render/math?math=W_p = \frac{Perceptual Score_p}{\sum^n_{i=1} Perceptual Score_i}">
 6. [Done in QGIS] Draw Predoninance Map
 
 ## Web-Based Visualisation
 In the Web-Based Visualisation, the images in KL_GSV are deleted since the size is too large, hence they are uploaded to MMU Google Drive. Download the images [here](https://drive.google.com/open?id=1F70rrxQ_MIAaTMxh9-CTY5jAw-VbpX57)
 
 Note: MMU Email is required to get access to download.
