# Sparse Deep Predictive Coding captures coutour integration capabilities of the early visual system
Victor Boutin, Angelo Franciosini, Frederic Chavane, Franck Ruffier, Laurent Perrinet

---

This github repository reproduces all the results of the paper entitled "Sparse Deep Predictive Coding captures contour integration capabilities of the early visual system" published at Plos Computational Biology ([ArXiv link here](https://arxiv.org/abs/1902.07651)).

This python repository is organized as follow : 
- The folder /SPC_PCB contains the package to run, train and evaluate the SDPC network.

- The folder /Savings contains most of the results of the simulation (so that you don't need to spend hours to retrain the network). When running the notebook, be carrefully to keep the variable 'Save' to False, otherwise it'll erase the previously saved results. All Figures are saved under the subfolder /Fig
- The notebooks:
    - The notebooks with a name starting with "1" are related to the training of the networks of the 2 tested databases (STL, CFD).
    - The notebook 2-Fig_1_S1_S2.ipynb is related to the generation of the Fig1, Fig S1 and Fig S2. All these figures are illustrated the learned RFs on the 2 different databases
    - The notebook 3-Fig3.ipynb is related to the generation of the Fig 3 (i.e the evolution of the sparsity relative to the feedback strenght)
    - The notebook 4-Fig_5_to_9_and_S3_and_S4.ipynb is related to the generation of the Association Field (with and without the relative feedback coloration)
    - The notebook 5-Fig_10_12_S5.ipynb is related to the figures showing the denoising abilites of the network, on natural images, and with different feedback strenght.
    - The notebook 6-Fig_11_13_S6.ipynb is related to the figures showing the denoising abilites of the network, on face databases, and with different feedback strenght.

## Overview of the main results 

### Architecture of a 2-layered SDPC model (Fig 1).

![Architecture of the SDPC](/Savings/Fig/Fig1/Fig1_tex.png "SDPC Architecture")

###  Results of training SDPC on the natural images and the face database (Fig 2) (see Notebook 2).

![Training results](/Savings/Fig/Fig2/Fig2_tex.png "SDPC features and reconstruction")
A) Randomly selected input images from the STL database. B) and F) : 16 randomly selected first-layer Receptive Fields. C) Input reconstruction made by the first layer. D) and G) 32 randomly selected second layer Receptive Fields. E) Input reconstruction made by the second layer.


###  Example of an association field (Fig 5)(see Notebook 4).

![Association Fields](/Savings/Fig/Fig5/Fig5_tex.png "Association Fields")
Example of a 9x9 interaction map of a V1 area centered on neurons strongly responding to a central preferred orientation of 30 deg. (A) Without feedback. (B) With a feedback strength equal to 1.  These interaction maps are obtained when the SDPC is trained on natural images. The color scale being saturated toward both maximum and minimum activity, all the activities above 0.8 or below 0.3 have the same color, respectively dark or white.


### Example of an association Fields colored with relative feedback (Fig 7) (see Notebook 4).

![Colored Association Fields](/Savings/Fig/Fig7/Fig7_tex.png "Colored Association Field")
Example of a 9x9 interaction map of a V1 area centered on neurons strongly responding to a central preferred orientation of 45 deg, and colored with the relative response w.r.t. no feedback. The feedback strength is set to 1 and the SDPC is trained on natural images. The color scale being saturated toward both maximum and minimum activity, all the activities above 1.3 or below 0.5 have the same color, respectively dark green or purple.

### Effect of the feedback strenght on the denoising abilities on natural images(Fig 10) (see Notebook 5).

![Denoising abilities](/Savings/Fig/Fig10/Fig10_tex.png "Denoising abilities")
Effect of the feedback strength on noisy images from natural images database. (A) In the left column, one image is corrupted by Gaussian noise of mean 0 and a standard deviation of 2. The central column exhibits the representations made by the first layer, and the right-hand column the representations made by the second layer. Within each of these blocks, the feedback strength is equal to 0 in the top line and 4 in the bottom line. (B) We plot the structural similarity index (higher is better) between original images and their representation by the first layer of the SDPC. (C) We plot the structural similarity index between original images and their representation by the second layer of the SDPC. All curves represent the median structural similarity index over 1200 samples of the testing set and present a logarithmic scale on the y-axis. The color code corresponds to the feedback strength, from grey for kFB to darker blue for higher feedback strength. The black line is the baseline, it is the structural similarity index between the noisy and original input images.


