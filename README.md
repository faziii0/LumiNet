# LumiNet

A Multi-Modal Feature Fusion Network for 3D Object Detection

# Code will be available Soon

<!-- 
![Fusion-new drawio](https://github.com/faziii0/LumiNet/assets/111413133/bfea5354-d194-4cfd-8ef4-138d72fb807f)
-->



# Environment Setup:
Linux (tested on Ubuntu 22.04)

Python 3.8

PyTorch 1.10 + CUDA-11.3




## Installation:

To deploy this project run

bash
git clone https://github.com/faziii0/LumiNet


bash
conda create -n liard python==3.8
conda activate liard
conda install pytorch==1.10.0 torchvision==0.11.0 torchaudio==0.10.cudatoolkit=11.3 -c pytorch -c conda-forge
conda install -c conda-forge cudatoolkit-dev
pip install -r requirements.txt
sh build_and_install.sh

## Depth Images
We use [MiDaS](https://github.com/isl-org/MiDaS) pretrained model to covert image_2 into depth images or download it from here Google. You can clone their repo and run this command
bash
python run.py --model_type dpt_beit_large_512 --input_path image_2 --output_path depth

## Dataset preparation:

Please download the official [KITTI 3D object detection](https://www.cvlibs.net/datasets/kitti/eval_object.php?obj_benchmark=3d) dataset and  train mask from [Epnet++](https://github.com/happinesslz/EPNetV2)


LiARD
├── data
│   ├── KITTI
│   │   ├── ImageSets
│   │   ├── object
│   │   │   ├── training
│   │   │   │   ├── calib
│   │   │   │   ├── velodyne
│   │   │   │   ├── label_2
│   │   │   │   ├── image_2
│   │   │   │   ├── depth
│   │   │   │   ├── train_mask
│   │   │   ├── testing
│   │   │   │   ├── calib
│   │   │   │   ├── velodyne
│   │   │   │   ├── image_2
│   │   │   │   ├── depth
├── lib
├── pointdep_lirad
├── tools


## Trained Model Evaluation





| Objects | Easy|Moderate     | Hard                   | 
| :-------- | :------- | :----------- | :----------|
| Car | 91.67% | 83.32% | 78.29%
| Pedestrian | 00.0% | 00.0% | 0.00%
| Cyclist | 00.0% | 00.0% | 00.0%

3D Predicted labels are avialable from the above Google


## Acknowledgements

 Thanks to all the contributors and authors of the project [PointRCNN](https://github.com/sshaoshuai/PointRCNN), [EPNet++](https://github.com/happinesslz/EPNetV2), [EPNet](https://github.com/happinesslz/EPNet),[MiDaS](https://github.com/isl-org/MiDaS)

## Citation
