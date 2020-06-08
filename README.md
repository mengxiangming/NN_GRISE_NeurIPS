# NN-GRISE - Code for reproducibility

We will demonstrate how to genreate data for a binary model and then learn it using NN-GRISE

## Data generation

Samples are generated using Julia and written to disk.

General graphical models can be created using the `FactorGraph` data structure and it can be sampled from using `raw_sampler_Potts`. 

Run the `data_gen.jl` script to generate samples for the binary model considered in the paper.
The data is written to `samples.csv`

## Learning with NN_GRISE

Learning is done using Tensorflow. This is best done on a GPU. Testing was done on a GTX 1050.

Run `learn.py` to do NN-GRISE on the saved samples. This script will learn, sample and calulate the error in TV and display it

The hyperparamters of NN-GRISE model can be changed in this scipt.

## Stucture Learning

The code demonstrating structure learning is inside the `Strucutre Learning` folder. This is a jupyter notebook learning the fifth order model discussed in the supplementary material. Running this requires the NetworkX python library [1].


[1] Hagberg, Aric, Pieter Swart, and Daniel S Chult. Exploring network structure, dynamics, and function using NetworkX. No. LA-UR-08-05495; LA-UR-08-5495. Los Alamos National Lab.(LANL), Los Alamos, NM (United States), 2008.
