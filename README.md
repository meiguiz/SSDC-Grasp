# SSDC-Grasp
Code for paper “SSDC-Grasp: A Joint Semantic Segmentation and Depth Completion Approach for Robotic Grasping of Transparent Objects”
> Ling Tong, Kechen Song, Member, IEEE, Hongkun Tian, Yi Man, Fiqi Sun, Youwei Chen, Yunhui Yan, and Qinggang Meng, Senior Member, IEEE. 

[图片6](https://github.com/meiguiz/SSDC-Grasp/assets/90629126/bb980c86-baf3-4051-b160-58d5a3e4661c)

## SSNet
---

The code of SSNet can be found at [code](https://drive.google.com/drive/folders/1LOUslijtms0wpNI_wNRVJ4iBi0kTV_a0?usp=drive_link) 

## DCNet
---
The video of robotic experiments can be found at [this](https://youtu.be/aDSG2khDXCA). 

The video of 6-Dof robotic grasp experiments can be found at [this](https://youtu.be/aDSG2khDXCA). 

Our test set used in grasp detection experimentson [Test set](https://github.com/meiguiz/SG-Grasp) 


## Getting Started
---


### Train

To train DCNet on the TranscCG dataset. 
```
$ python train.py --cfg [Configuration File]
```


### Evaluation

To evaluate DCNet on the TranscCG dataset
```
$ python test.py --cfg [Configuration File]
```


### Visualization

To visualize the inference results of DCNet on the TranscCG dataset. Change the config and checkpoint in inference.yaml, input dirs in sample_inference.py to your path.
```
$ python sample_inference.py 
```

### Grasp detection

---
Using TF-grasp [code](https://github.com/WangShaoSUN/grasp-transformer) or other methods. Use the result of SSNet and DCNet as input rgb and depth, then predict the grasping pose.
