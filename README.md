# AI-based Detection of Dairy Adulteration

This repository contains code to replicate results from the 2020 paper "Artificial intelligence-based identification of butter variations as a model study for detecting food adulteration".

### Packages
* Python 3.6.9
* Keras>=2.2.4
* Librosa
* Numpy, Pandas, Matplotlib


### Steps for training and testing
1- recordings folder: raw recordings without any processing

2- use data_to_npz.ipynb for data preprocessing
* amplitudes of recordings in “recordings” are normalized, and new records are saved in a folder named “normalized_recordings”
* 2-second chunks are created from normalized recordings (one-third of cheese recordings will be exported randomly)
* obtain shuffled train-valid and test sets as .npz files (80% for training, 10% for validation, and 10% test)

3- for CRNN model, run CRNN_MFCCs_withCV.ipynb
* It will save accuracy-loss results for each training within a folder named “npz_files_results”
* It will save .h5 models for each training in a folder named “models”

4- for Parallel CNN-RNN model, run Parallel_CNN_RNN_MFCCs_withCV.ipynb
* It will save accuracy-loss results for each training within a folder named “npz_files_results”
* It will save .h5 models for each training in a folder named “models”

5- test_recordings folder (for recordings collected via smartphone): raw recordings without any processing

6- for any inference raw file, do step 2.
* Npz file named “exampleinference_test_arr_MFCCs.npz” will be created.

		

