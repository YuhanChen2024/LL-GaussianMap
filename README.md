# :fire: LL-GaussianMap: Zero-shot Low-Light Image Enhancement via 2D Gaussian Splatting Guided Gain Maps
### :fire: :fire: LL-GaussianMap
- :star: - :point_right: [Arxiv](https://arxiv.org/abs/2601.15766)
- :star: - :point_right: [DATESET LOL](https://daooshee.github.io/BMVC2018website/) :point_right:[DATESET LSRW](https://github.com/JianghaiSCU/R2RNet) :point_right:[DATESET LoLI-Street](https://github.com/tanvirnwu/TriFuse_ACCV_2024) :point_right:[Train Data](https://github.com/Li-Chongyi/Zero-DCE) 
- :soon: - <strong>The code will be released soon</strong>

## Abstract

<img src="https://github.com/YuhanChen2024/LL-GaussianMap/blob/main/imgs/1.png" alt="my" width="1000" style="display: block; margin: 0 auto;"/>

Significant progress has been made in low-light image enhancement with respect to visual quality. However, most existing methods primarily operate in the pixel domain or rely on implicit feature representations. As a result, the intrinsic geometric structural priors of images are often neglected. 2D Gaussian Splatting (2DGS) has emerged as a prominent explicit scene representation technique characterized by superior structural fitting capabilities and high rendering efficiency. Despite these advantages, the utilization of 2DGS in low-level vision tasks remains unexplored. To bridge this gap, <strong>LL-GaussianMap is proposed as the first unsupervised framework incorporating 2DGS into low-light image enhancement.</strong> Distinct from conventional methodologies, the enhancement task is formulated as a gain map generation process guided by 2DGS primitives. The proposed method comprises two primary stages. First, high-fidelity structural reconstruction is executed utilizing 2DGS. Then, data-driven enhancement dictionary coefficients are rendered via the rasterization mechanism of Gaussian splatting through an innovative unified enhancement module. This design effectively incorporates the structural perception capabilities of 2DGS into gain map generation, thereby preserving edges and suppressing artifacts during enhancement. Additionally, the reliance on paired data is circumvented through unsupervised learning. Experimental results demonstrate that LL-GaussianMap achieves superior enhancement performance with an extremely low storage footprint, highlighting the effectiveness of explicit Gaussian representations for image enhancement.

## Getting Started
### Default Directory Structure
```
|---Train Dataset
|   |---1.jpg
|   |---2.jpg
|   |---....jpg
|---Test
|   |---1.jpg
|   |---2.jpg
|   |---....jpg
```
### Installation

1. Clone LL-GaussianImage
```bash
git clone --recursive https://github.com/YuhanChen2024/LL-GaussianImage
cd LL-GaussianImage
# git submodule update --init --recursive
```
2. Create the environment, here we show an example using conda.
```bash
conda create -n LL-GaussianImage python=3.10
conda activate LL-GaussianImage
# Please note that it is required to ensure python == 3.10, torch == 2.1.0, and cuda == 12.1
pip install torchvision==0.16.0 torchaudio==2.1.0
pip install constriction pandas pillow pytorch-msssim PyYAML tqdm ninja
pip install "opencv-contrib-python<4.12"
pip install "numpy<2"
cd gsplat2d
python setup.py build
python setup.py install
cd ..
```
### Train & Test

- :soon: - <strong>The code will be released soon</strong>

## Results on Low-light Image Enhancement

<img src="https://github.com/YuhanChen2024/LL-GaussianMap/blob/main/imgs/2.png" alt="my" width="1000" style="display: block; margin: 0 auto;"/>
<img src="https://github.com/YuhanChen2024/LL-GaussianMap/blob/main/imgs/3.png" alt="my" width="1000" style="display: block; margin: 0 auto;"/>
<img src="https://github.com/YuhanChen2024/LL-GaussianMap/blob/main/imgs/4.png" alt="my" width="1000" style="display: block; margin: 0 auto;"/>

## Citations

If you find this project helpful, please consider citing the following papers:

```
@misc{chen2026llgaussianmapzeroshotlowlightimage,
      title={LL-GaussianMap: Zero-shot Low-Light Image Enhancement via 2D Gaussian Splatting Guided Gain Maps}, 
      author={Yuhan Chen and Ying Fang and Guofa Li and Wenxuan Yu and Yicui Shi and Jingrui Zhang and Kefei Qian and Wenbo Chu and Keqiang Li},
      year={2026},
      eprint={2601.15766},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2601.15766}, 
}
```
