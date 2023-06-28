# ICCM: Instrument Classification in Carnatic Music
Instrument Classification in Carnatic Music (ICCM) is a project developed for the Music Technology Lab optional course, at Universitat Pompeu Fabra.

It aims to create a tool for musicologists, musicians and enthusiasts alike to identify the presence of some of the main instruments found in a Carnatic music performance (human voice, violin, mridangam).

This will be achieved through the training of several ML predictive models that will be able to classify each instrument, ultimately creating a graphical representation of the in and outs of each instrument through the length of a performance.

## Installation
### Prerequisites
- [Python v3.10.8](https://www.python.org/downloads/release/python-3108/) or [higher](https://www.python.org/downloads/)
- [Pip]([/src/Install_dataset.ipynb](https://pypi.org/project/pip/))
- [Jupyter Notebook](https://jupyter.org/install) (alternatively, [Google Colab](https://colab.research.google.com/?hl=es) can be used, but it's not recommended)

### Dependencies
All required dependencies and their respective versions are listed in [requirements.txt](requirements.txt). You can install all of them at once while on a command prompt environment located at the repository's top folder using the following command: `pip install -r requirements.txt`

### Machine Learning Pipeline
After installing the dependencies, you can now build the model yourself. To do so, download and install all the Jupyter Notebooks located at [/src/](/src/), following the next order:
  1) [Install_dataset.ipynb](/src/Install_dataset.ipynb)
  2) [Dataset_Creation.ipynb](/src/Dataset_Creation.ipynb)
  3) [Feature_Extraction.ipynb](/src/Feature_Extraction.ipynb)
  4) [Add_Instruments_To_Csv.ipynb](/src/Add_Instruments_To_Csv.ipynb)
  5) [Modelling.ipynb](/src/Modelling.ipynb)

## Procedure Details 
  1) **Install_dataset.ipynb**:

  Obtains the saraga1.5_carnatic dataset (16.2 GB) using the corresponding functions of the mir-data library. The download might take a long time depending on the connection. (If you already have access to the dataset, you may skip this step).

  2) **Dataset_Creation.ipynb**:

  Builds our dataset, using performances from saraga1.5_carnatic, which will be divided into small data/audio chunks and tagged by identifying silent regions for each instrument. These chunks and their respective instrument presence indicators will be referenced in a metadata dataframe (metadata.csv).

  3) **Feature_Extraction.ipynb**:

  Extracts the features from the audio chunks in a dataframe format (features.csv).
 
  4) **Add_Instruments_To_Csv.ipynb**:

  Adds a column to the features.csv dataframe with the instrument combination of each sample (0 for none of them, 1 for vocal only... 7 for all of them), so we later can swiftly create random sample sizes with equally represented instrument combinations.

  5) **Modelling.ipynb**:

  Trains and tests the Gradient Boosting Classifier models for each instrument.

## Future Improvements
Due to the limitations we had during this course, we haven't been able to complete the final result of this project, where an user would have been able to upload a carnatic music performance of their choice through a UI. A graphical representation of the in and outs of each instrument through the length of a performance would be displayed together with a audio player, so the user could test the result. [Here's an interactive prototype we made of the UI using Figma.](https://www.figma.com/proto/0VVCtlpFd2Nvckg7WiN1Eb/MTL--UI-Mockup?page-id=0%3A1&type=design&node-id=2-3&viewport=267%2C448%2C0.34&scaling=min-zoom&starting-point-node-id=2%3A3)

## Authors

- [Guillem Gauchia](https://github.com/GuillemGauchia)
- [Àlex Herrero](https://github.com/AlexHerreroDiaz)
- [Roddie McGuiness](https://github.com/Roddi01)
- [Gerard San Miguel](https://github.com/Dunxter)

## License
Distributed under the GPLv3 License. See [LICENSE](LICENSE) for more information.
