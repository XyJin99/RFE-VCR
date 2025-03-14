# RFE-VCR (ISPRS 2024)
### 📖[**Paper**](https://www.sciencedirect.com/science/article/abs/pii/S092427162400248X) | 🖼️[**PDF**](/figs/RFE-VCR.pdf)

PyTorch codes for "[RFE-VCR: Reference-enhanced transformer for remote sensing video cloud removal](https://www.sciencedirect.com/science/article/abs/pii/S092427162400248X)", **ISPRS Journal of Photogrammetry and Remote Sensing (ISPRS)**, 2024.

Authors: Xianyu Jin, [Jiang He*](https://jianghe96.github.io/), [Yi Xiao](https://xy-boy.github.io/), Ziyang Lihe, Xusi Liao, Jie Li, and Qiangqiang Yuan*<br>
Wuhan University

### Abstract
>As a novel data source for earth observation, satellite video can provide large-scale temporal information for dynamic monitoring. However, the cloud occlusion prevents satellite video from continuous and seamless observation of the earth’s surface. We propose the first satellite video cloud removal model RFE-VCR to approach this problem. In RFE-VCR, an efficient strategy of taking distant frames into training period is applied. A reference enhance block based on gated aggregation layers is proposed to explore the complementary information hidden in distant frames. A bidirectional local enhance block using deformable convolution is improved for feature refinement. Moreover, a decoupled temporal-spatial transformer is utilized for long-distance dependence modeling. Simulative and real experiments on Jilin-1 satellite videos demonstrate that our proposed network can achieve remarkable performance in video cloud removal task, as well as sensitive object hiding and high-reflection removal. More dynamic results of our experiments can be found at https://xyjin99.github.io/RFE-VCR/.

### Overall
 ![image](/figs/network.png)

## Dataset Preparation
We created a synthetic dataset named WHU-VCD based on the atmospheric scattering model with authentic cirrus cloud bands and satellite video scenes to simulate the motion characteristics of both thick and thin clouds in sub-second-level satellite videos.
Please download our dataset in 
 * Baidu Netdisk [WHU-VCD](https://pan.baidu.com/s/1sCXvKb_3HKq0xtvYx8y5Zg) Code: 5nhm
 * Zenodo: TODO

You can also train your dataset following the directory structure below!
### Data directory structure
train--  
&emsp;|&ensp;cloud--  
&emsp;&emsp;|&ensp;SCENE 000---  
&emsp;&emsp;&emsp;| 00000000.png  
&emsp;&emsp;&emsp;| ···.png  
&emsp;&emsp;&emsp;| 00000099.png     
&emsp;&emsp;|&ensp;SCENE N---  
&emsp;|&ensp;mask--  

eval--  
&emsp;|&ensp;cloud--  
&emsp;&emsp;|&ensp;SCENE 000---  
&emsp;&emsp;&emsp;| 00000000.png  
&emsp;&emsp;&emsp;| ···.png  
&emsp;&emsp;&emsp;| 00000099.png    
&emsp;&emsp;|&ensp;SCENE N---  
&emsp;|&ensp;mask--  

realtest--  
&emsp;|&ensp;cloud--  

## Training
```
TODO
```

## Evaluation
```
TODO
```

## Test
```
TODO
```

### Quantitative results
 ![image](/figs/quantitative.png)
### Qualitative results
 ![image](/figs/qualitative.png)
#### More details can be found in our paper and our https://xyjin99.github.io/RFE-VCR/ !


## Contact
If you have any questions or suggestions, feel free to contact me. 😊  
Email: jin_xy@whu.edu.cn

## Citation
If you find our work useful in your research, we would appreciate your citation. 😊😊
```
@article{jin2024rfe,
  title={RFE-VCR: Reference-enhanced transformer for remote sensing video cloud removal},
  author={Jin, Xianyu and He, Jiang and Xiao, Yi and Lihe, Ziyang and Liao, Xusi and Li, Jie and Yuan, Qiangqiang},
  journal={ISPRS Journal of Photogrammetry and Remote Sensing},
  volume={214},
  pages={179--192},
  year={2024},
  publisher={Elsevier}
}
```

## Acknowledgement
Our work is built upon [E2FGVI](https://github.com/MCG-NKU/E2FGVI) and [TimeSformer](https://github.com/facebookresearch/TimeSformer).
Thanks to the author for the source code !
