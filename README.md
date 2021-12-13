![logo](data/logo.png)

[![CodeFactor](https://www.codefactor.io/repository/github/everlookneversee/bts_dp_mri/badge)](https://www.codefactor.io/repository/github/everlookneversee/bts_dp_mri)
![GitHub](https://img.shields.io/github/license/EverLookNeverSee/BTS_DP_MRI)
![GitHub branch checks state](https://img.shields.io/github/checks-status/EverLookNeverSee/BTS_DP_MRI/main)
![GitHub language count](https://img.shields.io/github/languages/count/EverLookNeverSee/BTS_DP_MRI)
![GitHub top language](https://img.shields.io/github/languages/top/EverLookNeverSee/BTS_DP_MRI)
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/EverLookNeverSee/BTS_DP_MRI)
![Lines of code](https://img.shields.io/tokei/lines/github/EverLookNeverSee/BTS_DP_MRI)
![GitHub all releases](https://img.shields.io/github/downloads/EverLookNeverSee/BTS_DP_MRI/total)
![GitHub issues](https://img.shields.io/github/issues-raw/EverLookNeverSee/BTS_DP_MRI)
![GitHub pull requests](https://img.shields.io/github/issues-pr-raw/EverLookNeverSee/BTS_DP_MRI)
![GitHub release (latest by date)](https://img.shields.io/github/v/release/EverLookNeverSee/BTS_DP_MRI)
![GitHub contributors](https://img.shields.io/github/contributors/EverLookNeverSee/BTS_DP_MRI)
![GitHub last commit](https://img.shields.io/github/last-commit/EverLookNeverSee/BTS_DP_MRI)

## Authors
* Research: [Dr. Golestan Karami](https://www.linkedin.com/in/golestan-karami-45984938/)
* Development: [Milad Sadeghi DM](https://elns.ir)


## Sample Pipeline
**Pre-processing:**  
Desired dataset structure:  
```
.
└── Train
    ├── 001
    │   ├── 001-Ann.nii
    │   ├── 001-MD.nii
    │   ├── 001-rCBV.nii
    │   └── 001-T1.nii
    ├── 002
    │   ├── 002-Ann.nii
    │   ├── 002-MD.nii
    │   ├── 002-rCBV.nii
    │   └── 002-T1.nii
```
Do preprocessing on dataset:
```shell
python preprocessing.py --verbose --dataset <path to dataset directory>
```
This will create a new directory called *npy_files*, then creates specific folders for
each sample we have in dataset and saves image.npy and ann.py files in these folders.
```
npy_files/
├── 0
│   ├── ann_0.npy
│   └── image_0.npy
├── 1
│   ├── ann_1.npy
│   └── image_1.npy
```


## License
This project licensed under the MIT License - see the [LICENSE](LICENSE) file for more details.


## References
1. [Optimized U-Net for Brain Tumor Segmentation](https://arxiv.org/abs/2110.03352)
2. [Optimized High Resolution 3D Dense-U-Net Network for Brain and Spine Segmentation](https://www.mdpi.com/2076-3417/9/3/404)
3. [A novel fully automated MRI-based deep-learning method for classification of IDH mutation status in brain gliomas](https://pubmed.ncbi.nlm.nih.gov/31637430/)
