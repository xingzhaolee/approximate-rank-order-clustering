# Approximate Rank-Order Clustering (AROC)
Implementation of Approximate Rank-Order Clustering (AROC) algorithm in [[1604.00989] Clustering Millions of Faces by Identity](https://arxiv.org/abs/1604.00989). Features used in the implementation can be found at [face_verification_experiment](https://github.com/AlfredXiangWu/face_verification_experiment/raw/master/results/LightenedCNN_C_lfw.mat).

Note:
- Features extracted by any models can be used
- FLANN is can be swapped out for other k-nn methods

| | F-measure |
| :---: | :---: |
| This implementation | ~0.88 |
| Reported | 0.87 |

## Instructions
```bash
mkdir extracted-features

# Download the LFW features from face_verification_experiment by AlfredXiangWu
wget https://github.com/AlfredXiangWu/face_verification_experiment/raw/master/results/LightenedCNN_C_lfw.mat -P extracted-features

# Perform the clustering
python main.py
```

## Requirements
- python3
- numpy
- scipy
- pyflann

```bash
conda create -n aroc
conda activate aroc
conda install numpy pyflann scipy
```
