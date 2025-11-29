# MVDNet_code
A precise berry counting method for in-cluster grapes to guide berry thinning

The proposed methodology comprises two core components: a dual-branch network and a post-processing algorithm. First, to address the challenges posed by small berry size, significant occlusion, and complex environmental interference during the berry thinning period, a lightweight network named MVDNet was designed, which balances high accuracy and dual-task performance. This network simultaneously performs berry density map regression and grape cluster segmentation. The input images are processed through the dual-branch multi-task network to generate a density map of grape berries and a preliminary segmentation mask of the grape clusters. Subsequently, a post-processing algorithm refines the segmentation mask to achieve instance-level separation and precise localization of individual grape clusters. Within each segmented cluster region, the number of berries is calculated by integrating the density map, enabling accurate berry counting per cluster. This method can be applied to vineyards in complex environments, providing a reliable and efficient technical solution for automated berry thinning.

If you want to train the model, you must prepare the dataset. You can see the path MVDNet_code\data..., you must prepare point map, images, mask images, and text for dataset splitting, then you can use train.py to train the model. You can use post_process.py to get berry number in-cluster grape.

Our code is developed based on NWPU-Crowd Sample Code, you may cite:

```
@article{gao2020nwpu,
  title={NWPU-Crowd: A Large-Scale Benchmark for Crowd Counting and Localization},
  author={Wang, Qi and Gao, Junyu and Lin, Wei and Li, Xuelong},
  journal={IEEE Transactions on Pattern Analysis and Machine Intelligence},
  doi={10.1109/TPAMI.2020.3013269},
  year={2020}
}
```
