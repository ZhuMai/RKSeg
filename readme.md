# RKSeg


This repository is for [Semantic Segmentation of Medical Images Based on Runge–Kutta Methods](https://doi.org/10.3390/bioengineering10050506).

### citation
If you find RKSeg useful for your research, please consider citing:

    @Article{bioengineering10050506,
    AUTHOR = {Zhu, Mai and Fu, Chong and Wang, Xingwei},
    TITLE = {Semantic Segmentation of Medical Images Based on Runge&ndash;Kutta Methods},
    JOURNAL = {Bioengineering},
    VOLUME = {10},
    YEAR = {2023},
    NUMBER = {5},
    ARTICLE-NUMBER = {506},
    URL = {https://www.mdpi.com/2306-5354/10/5/506},
    ISSN = {2306-5354},
    ABSTRACT = {In recent years, deep learning has achieved good results in the semantic segmentation of medical images. A typical architecture for segmentation networks is an encoder&ndash;decoder structure. However, the design of the segmentation networks is fragmented and lacks a mathematical explanation. Consequently, segmentation networks are inefficient and less generalizable across different organs. To solve these problems, we reconstructed the segmentation network based on mathematical methods. We introduced the dynamical systems view into semantic segmentation and proposed a novel segmentation network based on Runge&ndash;Kutta methods, referred to hereafter as the Runge&ndash;Kutta segmentation network (RKSeg). RKSegs were evaluated on ten organ image datasets from the Medical Segmentation Decathlon. The experimental results show that RKSegs far outperform other segmentation networks. RKSegs use few parameters and short inference time, yet they can achieve competitive or even better segmentation results compared to other models. RKSegs pioneer a new architectural design pattern for segmentation networks.},
    DOI = {10.3390/bioengineering10050506}
    }

We implement RKSegs based on [MIC-DKFZ/nnUNet](https://github.com/MIC-DKFZ/nnUNet/tree/nnunetv1). You can copy our code into the nnUNet framework for training.

Example of training RKSeg-L for 150 epochs on Task004_Hippocampus:

```bash
nnUNet_train 2d RKSegLTrainerV2_noDeepSupervision_150epochs 4 0
```

Example of training RKSeg-R for 150 epochs on Task004_Hippocampus:

```bash
nnUNet_train 2d RKSegRTrainerV2_noDeepSupervision_150epochs 4 0
```


