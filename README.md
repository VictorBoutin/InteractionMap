# Sparse Deep Predictive Coding captures coutour integration capabilities of the early visual system
Victor Boutin, Angelo Franciosini, Frederic Chavane, Franck Ruffier, Laurent Perrinet

---

This github repository reproduces all the results of the paper entitled "Sparse Deep Predictive Coding captures contour integration capabilities of the early visual system" published at Plos Computational Biology ([ArXiv link here](https://arxiv.org/abs/1902.07651)).

This python repository is organized as follow : 
- The folder /SPC_PCB contains the package to run, train and evaluate the SDPC network.
- The folder /Savings contains most of the results of the simulation (so that you don't need to spend hours to retrain the network). When running the notebook, be carrefully to keep the variable 'Save' to False, otherwise it'll erase the previously saved results
- The notebooks:
    - The notebooks with a name starting with "1" are related to the training of the networks of the 2 tested databases (STL, CFD).
    - The notebooks with a name starting with "2" are related to the generation of Fig2, Fig3 (only for CFD database), Fig4 and Fig6 (see overview of the main results). Note that we did not upload all the simulation files to limit the size of the repository. If one want to reproduce all the figures of the paper, one need to regenerate the .pkl file using paramters describe in the Table 1 of the paper (this can be esaily done with the notebooks having name starting with "1").
    - The notebooks with a name sarting with "3" are related to the generation of the supplementary materials figure for all tested databases. The notebook called "3-CFD_Fig7_and_SD" is also used to generate the Fig 7 of the paper.
    - The notebook called "4-Fig5.ipynb" is used to generate the figure 5 from the paper. Note that we have conducted this analysis only on the STL database
    - The notebook called "5-Table2-SurfaceCoverage" is used to generate the Table2 of the paper.
