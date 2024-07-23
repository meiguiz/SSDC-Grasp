# SSDC-Grasp
Code for paper “SSDC-Grasp: A Joint Semantic Segmentation and Depth Completion Approach for Robotic Grasping of Transparent Objects”
> Ling Tong, Kechen Song, Member, IEEE, Hongkun Tian, Yi Man, Fiqi Sun, Youwei Chen, Yunhui Yan, and Qinggang Meng, Senior Member, IEEE. 

![图片6](https://github.com/meiguiz/SSDC-Grasp/assets/90629126/fac8854e-e88d-4d60-8a9d-5694e2b70144)

## SSNet
---

The code of SSNet can be found at [code](https://github.com/meiguiz/SG-Grasp). Or you can use other semantic segmentation methods from MMSegmentation at [this](https://github.com/open-mmlab/mmsegmentation).

## DCNet
---
The video of 4-Dof robotic experiments can be found at [this](https://youtu.be/aDSG2khDXCA). 


Our test set used in grasp detection experimentson [Test set](https://drive.google.com/drive/folders/1LOUslijtms0wpNI_wNRVJ4iBi0kTV_a0?usp=drive_link) 


## Getting Started
---


### Train

To train DCNet on the TransCG dataset. 
```
$ python train.py --cfg [Configuration File]
```


### Evaluation

To evaluate DCNet on the TransCG dataset
```
$ python test.py --cfg [Configuration File]
```


### Visualization

To visualize the inference results of DCNet on the TransCG dataset. Change the config and checkpoint in inference.yaml, input dirs in sample_inference.py to your path.
```
$ python sample_inference.py 
```

### Grasp detection

---
Using TF-grasp [code](https://github.com/WangShaoSUN/grasp-transformer) or other grasp detection methods. Use the result of SSNet and DCNet as input rgb and depth, then predict the grasping poses.

### Acknowledgement

Code heavily inspired and modified from [code](https://github.com/Galaxies99/TransCG)

