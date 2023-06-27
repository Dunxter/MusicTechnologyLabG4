# ICCM: Instrument Classification in Carnatic Music
Instrument Classification in Carnatic Music (ICCM) is a project developed for the Music Technology Lab optative course, at Universitat Pompeu Fabra.

It aims to create a tool for musicologists, musicians and enthusiasts alike to identify and visualize the presence of the main instruments found in Carnatic music tradition (human voice, violin, tanbura and mridangam) in a piece of the user’s choice. 

This will be achieved through the training of a ML predictive model that will be able to classify each instrument, ultimately creating a graphical representation of the in and outs of each instrument through the length of a performance.

In order to use this model you must follow the following steps:

  1) Download and execute the code Install_dataset.ipynb in jupyter notebook  to obtain the saraga1.5_carnatic dataset (16.2 GB) using the corresponding functions of the mir-data library. The download might take a long time depending on the connection. (If you already have the dataset you can skip this step)
  2) Download and run step by step the Dataset_Creation.ipynb code to transform the saraga1.5_carnatic dataset into .wav chunks and obtain the data information that identifies what kind of instruments appear or if there is silence.
  3) Download and execute step by step the code Feature_Extraction.ipynb to extarct the features from the chunks in a .csv format (If you already have a file with the features of your dataset in the corresponding format this step is not necessary).
  4) Download and run step by step the Modelling.ipynb code to create a ML model and see the results.
