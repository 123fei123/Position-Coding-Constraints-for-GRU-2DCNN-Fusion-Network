# Position-Coding-Constraints-for-GRU-2DCNN-Fusion-Network
Code implementation for the paper "An Elastic Parametric Seismic Inversion Method with Position Coding Constraints for GRU-2DCNN Fusion Network". This repository contains GRU-2DCNN forward and inverse model modules with position coding constraints, along with model data for reproducing the elastic parameter inversion results presented in the paper.

This code implements a neural network constrained by seismic facies information for elastic parameter inversion of pre-stack seismic data. This method effectively improves the stability, physical rationality and lateral continuity of the inversion results by introducing phase consistency constraints into the deep learning framework.
It has three main characteristics: (1). End-to-end elastic parameter inversion based on deep neural networks. (2). Integrating positional encoding with seismic data to achieve facies-controlled constraints. (3). Applicability to pre-stack seismic inversion under the condition of limited logging data.
The entire inversion workflow consists of the following three core modules:
Phase-controlled constraint module: The seismic facies classification results are first transformed into fixed-dimension word embeddings, which are then further processed using positional coding to generate phase-coded. Finally, the seismic data, position coding, and phase-coded are concatenated as input to the neural network, thereby incorporating seismic facies as a constraint within the inversion process. 
Neural network inversion module: Convolutional neural networks, gated recurrent units, and self-attention mechanism are integrated to invert elastic parameters from pre-stack seismic data.
Forward modeling module:
The inverted elastic parameters are converted into synthetic seismic data using an AVO convolutional model. The synthetic seismic data are then compared with the real seismic data to compute the seismic data loss.
The code is divided into two independent runs, one is the NO_Seismic phase constrained inversion, and the other is the Seismic phase constrained inversion, which can be run directly in turn.
Requirements
•	Python ≥ 3.8
•	NumPy
•	TensorFlow
•	Matplotlib
Data Availability
•	The example seismic data and well log data provided in this repository are all synthetic and are intended solely for method demonstration and testing purposes.
Code Availability Statement
•	All code used in this study is open source and has been publicly released in this repository.
•	Reproduction of the experimental results does not require any proprietary software.


