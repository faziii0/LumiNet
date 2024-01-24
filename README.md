# LiARD+++
A Multi-Modal Feature Fusion Network for 3D Object Detection

# Code will be available Soon


![Fusion-new drawio](https://github.com/faziii0/LiARD/assets/111413133/bce1d434-21bc-4aa1-86ed-14e080e8d90f)

Environment:
Linux (tested on Ubuntu 22.04)
Python 3.8
PyTorch 1.10 + CUDA-11.3

# Clone Repo:
   git clone https://github.com/faziii0/LiARD

# Installation:
  1. conda create -n liard python==3.8
  2. conda activate liard
  3. conda install pytorch==1.10.0 torchvision==0.11.0 torchaudio==0.10.0 cudatoolkit=11.3 -c pytorch -c conda-forge
  4. conda install -c conda-forge cudatoolkit-dev
  5. pip install -r requirements.txt
  6. sh build_and_install.sh

# Dataset preparation:
Please download the official KITTI 3D object detection dataset and  train mask from Epnet++

LiARD
├── data
│   ├── KITTI
│   │   ├── ImageSets
│   │   ├── object
│   │   │   ├──training
│   │   │      ├──calib & velodyne & label_2 & image_2 & depth_image & train_mask
│   │   │   ├──testing
│   │   │      ├──calib & velodyne & image_2 & depth_image
├── lib
├── point_depth
├── tools

# Trained model
