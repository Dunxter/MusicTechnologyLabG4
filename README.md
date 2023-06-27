# ICCM: Instrument Classification in Carnatic Music
Instrument Classification in Carnatic Music (ICCM) is a project developed for the Music Technology Lab optative course, at Universitat Pompeu Fabra.

It aims to create a tool for musicologists, musicians and enthusiasts alike to identify and visualize the presence of the main instruments found in Carnatic music tradition (human voice, violin, tanbura and mridangam) in a piece of the user’s choice. 

This will be achieved through the training of a ML predictive model that will be able to classify each instrument, ultimately creating a graphical representation of the in and outs of each instrument through the length of a performance.

In order to build this model yourself you must follow the following steps:

  1) Download and execute the Install_dataset.ipynb jupyter notebook to to obtain the saraga1.5_carnatic dataset (16.2 GB) using the corresponding functions of the mir-data library. The download might take a long time depending on the connection. (If you already have access to the dataset you may skip this step).
  2) Download and run step by step the Dataset_Creation.ipynb notebook to build our dataset, using performances from saraga1.5_carnatic, which will be divided into small data/audio chunks and tagged by identifying silent regions for each instrument. These chunks and their respective instrument presence indicators will be referenced in a metadata dataframe (metadata.csv).
  4) Download and run all the Feature_Extraction.ipynb notebook to extract the features from the audio chunks in a dataframe format (features.csv)
  5) Download and execute the Modelling.ipynb notebook to build and test the models for each instrument.
