# IoT Intrusion Detection System using Dimensionality Reduction Techniques
The project aims to investigate the impact of dimensionality reduction techniques on the accuracy and performance of machine learning-based intrusion detection systems in IoT environments.

# Introduction
Intrusion detection systems (IDS) are essential for ensuring the security of IoT systems. However, traditional IDS techniques are not suitable for IoT environments due to the high-dimensional nature of IoT data. In this project, we explore the impact of dimensionality reduction techniques on the accuracy and performance of machine learning-based IDS in IoT environments.

# Dependencies
The following dependencies are required to run the program:
- Python 3.8.4.
- Numpy 1.23.5.
- Pandas 1.5.3.
- Scikit-learn 1.2.2.
- umap-learn 0.5.3.
- Matplotlib 3.7.1.
- numpyencoder 0.3.0.

Please note that our tests were performed using the above versions of the dependencies (also set in the file `requirements.txt`). However, the program should work with other versions of the dependencies as well.

# Installation
Clone the repository :` git clone git@github.com:cchohra/ImpactOfDRonIDSinIoT.git` <br />
Install the dependencies :` pip install -r requirements.txt`

# Project Structure
The project is structured as follows:
- `requirements.txt` : Contains the dependencies required to run the program.
- `preprocessing.py` : Contains the functions for preprocessing the data and dimensionality reduction. The functions are used in the main file. The preprocessing function include the following tasks :
    - Encoding the categorical features.
      - Convert IP adress to unsigned 32 bits integers.
      - Convert dates to timestamps (seconds since 1970-01-01 00:00:00 UTC).
    - Scaling the features.
    - Handling NaN and NULL values.
    - Performing dimensionality reduction using various techniques and save resulted data in other ".npy" files. The techniques used for dimensionality reduction are :
      - Principal Component Analysis (PCA).
      - Linear Discriminant Analysis (LDA).
      - Uniform Manifold Approximation and Projection (UMAP).
- `visualization.py` : Contains the functions for visualizing the results.
- `main.py` : The main file that runs the program, this file performs the following tasks:
    - Load the dataset.
    - Preprocess the data and perform dimensionality reduction using various techniques.
    - Define several machine learning models to classify the data. The tested models are :
      - Logistic Regression.
      - Decision Tree.
      - Support Vector Machine.
      - Multilayer Perceptron (neural network).
    - Use cross-validation to evaluate the performance of each model on the original and reduced data.
    - Generate figures to visualize the results.
    - Save the metrics in a pickle and a json file.

The project also contains the following folders that are not shared on GitHub due to their large size:
- `data` : Contains the original dataset (`dataset.csv`) and the reduced datasets. The reduced datasets are generated by the program on the first run (if they do not exist already) and are saved in the folder.
- `figures` : Contains the figures generated by the program.
- `metrics` : Contains the metrics generated by the program.
  - `metrics.pkl` : Contains the metrics in pickle format.
  - `metrics.json` : Contains the metrics in json format.

At the exception of the `dataset.csv` file which can be downloaded from [our drive](https://drive.google.com/file/d/1jWeCw8Vi5KiRQN-m8qfGE5hhwbWxYgUi/view?usp=sharing) or from the original creator of the dataset [webpage](https://sites.google.com/view/iot-network-intrusion-dataset/home), all the other files can be generated by the program, the program will test if the files exist and only generate them if they do not.

Reduction the dimensionality with UMAP is very time consuming, so we recommend to use the reduced datasets that we generated and shared on [our drive](https://drive.google.com/file/d/1jWeCw8Vi5KiRQN-m8qfGE5hhwbWxYgUi/view?usp=sharing) if you want to rapidely test the program.

# Usage
Please follow the following steps to run the program:
- Download the `data` folder from [our drive](https://drive.google.com/file/d/1jWeCw8Vi5KiRQN-m8qfGE5hhwbWxYgUi/view?usp=sharing) and place it in the root of the project.
- Run the main.py file :` python main.py`.
- Depending on your configuration, the program may take several hours to run generate all the results, but we have added some messages to help you keep track of the progress.
- You will find the results in the `figures` and `metrics` folders.
- Please consider removing the reduced datasets from the `data` folder if you want to regenerate them. The same goes for the metrics.

# Dataset
We used the IoTID20 dataset for this project. The dataset can be downloaded from [here](https://sites.google.com/view/iot-network-intrusion-dataset/home). To have a better understanding of the dataset, please refer to the [paper](https://link.springer.com/chapter/10.1007/978-3-030-47358-7_52) that introduced it.

# Results
You can find the results in the `figures` and `metrics` folders. We will publish our interpretation of the results once the paper is peer-reviewed.

# Conclusion
We will publish our conclusion once the paper is peer-reviewed.

# License
This project is licensed under the [MIT License](https://fr.wikipedia.org/wiki/Licence_MIT).

# Acknowledgments
We would like to thank the creators of the [IoTID20](https://sites.google.com/view/iot-network-intrusion-dataset/home) dataset for making it publicly available.
