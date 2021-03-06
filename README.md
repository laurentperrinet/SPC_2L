# Effect of top-down connections in Hierarchical sparse coding

This github repository reproduces all the results of the paper entitled "Effect of top-down connections in Hierarchical sparse coding" published at Neural Computaiton ([ArXiv link here](https://arxiv.org/abs/2002.00892)).

This python repository is organized as follow : 
- The folder /SPC_2L contains the package where the network 2L-SPC network, its training, and all necessary tools are coded.
- The folder /Savings contains most of the results of the simulation (so that you don't need to spend hours to retrain the network). When running the notebook, be carrefully to keep the variable 'Save' to False, otherwise it'll erase the previously saved results
- The notebooks:
    - The notebooks with a name starting with "1" are related to the training of the networks of the 4 tested databases ( ATT, MNIST, STL, CFD).
    - The notebooks with a name starting with "2" are related to the generation of Fig2, Fig3 (only for CFD database), Fig4 and Fig6 (see overview of the main results). Note that we did not upload all the simulation files to limit the size of the repository. If one want to reproduce all the figures of the paper, one need to regenerate the .pkl file using paramters describe in the Table 1 of the paper (this can be esaily done with the notebooks having name starting with "1").
    - The notebooks with a name sarting with "3" are related to the generation of the supplementary materials figure for all tested databases. The notebook called "3-CFD_Fig7_and_SD" is also used to generate the Fig 7 of the paper.
    - The notebook called "4-Fig5.ipynb" is used to generate the figure 5 from the paper. Note that we have conducted this analysis only on the STL database
    - The notebook called "5-Table2-SurfaceCoverage" is used to generate the Table2 of the paper.
    
    
## Overview of the main results 

### Top-down connection allows a mitigation of the prediction error (Fig 2).
Results on CFD database when varying the first layer sparsity (see arXiv paper for other database and also the effect of varying the second layer sparsity):
![Prediction Breakdown on CFD when varying lbda1](/Savings/Fig/Fig2-a-ii.png "Prediction breakdown when varying the first layer sparsity")

### Top-down connection allows a faster convergence of the inference process (Fig 4).
Results on CFD database when varying the first and the second layer sparsity (see arXiv paper for other databases:
![Number of inference iteration on CFD when varying lbda1 and lbda2](/Savings/Fig/Fig4-a_and_b-ii.png "Number of inference iteration")


### Top-down connection refines the prediction made by the second layer (Fig 5).
Results on STL :
![Evolution of prediction error with iteration](/Savings/Fig/Fig5-a.png "Evolution of prediction error with iteration")

### Top-down connection speeds-up the training of the network (Fig 6).
Results on CFD database (see arXiv paper for other database):
![Training on CFD database](/Savings/Fig/Fig6-ii.png "Training on CFD database")


### Top-down connections allows the learning of extended and more contextual RFs (Fig 7).
![Activation and features for Hila and 2LSPC](/Savings/Fig/Fig7.png "Activation and features for HiLa and 2LSPC")
