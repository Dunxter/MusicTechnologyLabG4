# ICCM: Instrument Classification in Carnatic Music
Instrument Classification in Carnatic Music (ICCM) is a project developed for the Music Technology Lab optative course, at Universitat Pompeu Fabra.

It aims to create a tool for musicologists, musicians and enthusiasts alike to identify and visualize the presence of the main instruments found in Carnatic music tradition (human voice, violin, tanbura and mridangam) in a piece of the user’s choice. 

This will be achieved through the training of a ML predictive model that will be able to classify each instrument, ultimately creating a graphical representation of the in and outs of each instrument through the length of a performance.

## Installation
All dependencies and their respective versions are listed in [requirements.txt](requirements.txt). You can install all of them at once while on a command prompt environment located at the repository's top folder using the following command: `pip install -r requirements.txt`

After installing all necessary dependancies, you can now build the model yourself. To do so, download and install all the Jupyter Notebooks located at [/src/](/src/), following the next order:
  1) [Install_dataset.ipynb](/src/Install_dataset.ipynb)
  2) [Dataset_Creation.ipynb](/src/Dataset_Creation.ipynb)
  3) [Feature_Extraction.ipynb](/src/Feature_Extraction.ipynb)
  4) [Add_Instruments_To_Csv.ipynb](/src/Add_Instruments_To_Csv.ipynb)
  5) [Modelling.ipynb](/src/Modelling.ipynb)

## Procedure Details 
  1) **Install_dataset.ipynb**:

  Obtains the saraga1.5_carnatic dataset (16.2 GB) using the corresponding functions of the mir-data library. The download might take a long time depending on the connection. (If you already have access to the dataset you may skip this step).

  2) **Dataset_Creation.ipynb**:

  Builds our dataset, using performances from saraga1.5_carnatic, which will be divided into small data/audio chunks and tagged by identifying silent regions for each instrument. These chunks and their respective instrument   presence indicators will be referenced in a metadata dataframe (metadata.csv).

  3) **Feature_Extraction.ipynb**:

  Extracts the features from the audio chunks in a dataframe format (features.csv).
 
 4) **Add_Instruments_To_Csv.ipynb**:

  Adds a column to the features.csv dataframe with the instrument combination of each sample (0 for none of them, 1 for vocal only... 7 for all of them), so we later can swiftly create random sample sizes with equally represented instrument combinations.

  5) **Modelling.ipynb**:

  Trains and tests the models for voice, violin and mridangam.
