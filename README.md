# Final Project of CSC249
Welcome to the final project of CSC249!

In this final project, you are going to build deep learning models for two tasks on A2D dataset. Please read *final_project.pdf* for more details of the project requirement.



## Preparation

Before start working on a specific task, please do the following preparation on your Google cloud.

- **Clone the repository**

  Please use the following command to clone this repository (please do not download the zip file):

  ```bash
  git clone --recursive https://github.com/rochesterxugroup/csc249_final_proj.git
  ```

  If there is any updates of the repository, please use the following command to pull:

  ```bash
  git pull --recurse-submodules
  ```

  cd to the cloned repo:

  ```bash
  cd csc249_final_proj
  ```

- **Environment Configuration**

  1. Download and install miniconda from https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh

  2. Install the virtual enviroment and its dependencies by:

     ```bash
     conda env create -f env.yml
     ```

  3. Activate the virtual environment by (please remember to activate virtual environment everytime you login on google cloud):

     ```bash
     conda activate pytorch_0_4_1
     ```

  4. Then, install Pytorch 0.4.1 and torchvision

     ```bash
     conda install pytorch=0.4.1 cuda92 -c pytorch
     conda install torchvision
     ```

- **Download A2D dataset**

  Please make sure you are at the `csc249_final_proj` directory.

  1. Download the A2D dataset

     ```bash
     curl http://web.eecs.umich.edu/\~jjcorso/bigshare/A2D_main_1_0.tar.bz --output A2D_main_1_0.tar.bz
     ```

  2. Decompress the tar ball and rename the folder

     ```bash
     tar xvf A2D_main_1_0.tar.bz
     mv Release A2D
     ```

  3. Extract frames from videos

     ```bash
     python extract_frames.py
     ```

