# MobileMamba

--- 
Official PyTorch implementation of "[**MobileMamba: Lightweight Multi-Receptive Visual Mamba Network**](https://arxiv.org/pdf/2411.15941)".

[Haoyang He<sup>1*</sup>](https://scholar.google.com/citations?hl=zh-CN&user=8NfQv1sAAAAJ),
[Jiangning Zhang<sup>2*</sup>](https://zhangzjn.github.io),
[Yuxuan Cai<sup>3</sup>](https://scholar.google.com/citations?hl=zh-CN&user=J9lTFAUAAAAJ),
[Hongxu Chen<sup>1</sup>](https://scholar.google.com/citations?hl=zh-CN&user=uFT3YfMAAAAJ)
[Xiaobin Hu<sup>2</sup>](https://scholar.google.com/citations?hl=zh-CN&user=3lMuodUAAAAJ),

[Zhenye Gan<sup>2</sup>](https://scholar.google.com/citations?user=fa4NkScAAAAJ&hl=zh-CN),
[Yabiao Wang<sup>2</sup>](https://scholar.google.com/citations?user=xiK4nFUAAAAJ&hl=zh-CN),
[Chengjie Wang<sup>2</sup>](https://scholar.google.com/citations?hl=zh-CN&user=fqte5H4AAAAJ),
Yunsheng Wu<sup>2</sup>,
[Lei Xie<sup>1†</sup>](https://scholar.google.com/citations?hl=zh-CN&user=7ZZ_-m0AAAAJ)

<sup>1</sup>College of Control Science and Engineering, Zhejiang University, 
<sup>2</sup>Youtu Lab, Tencent,
<sup>3</sup>Huazhong University of Science and Technology
> **Abstract:** Previous research on lightweight models has primarily focused on CNNs and Transformer-based designs. CNNs, with their local receptive fields, struggle to capture long-range dependencies, while Transformers, despite their global modeling capabilities, are limited by quadratic computational complexity in high-resolution scenarios. Recently, state-space models have gained popularity in the visual domain due to their linear computational complexity. Despite their low FLOPs, current lightweight Mamba-based models exhibit suboptimal throughput.
In this work, we propose the MobileMamba framework, which balances efficiency and performance. We design a three-stage network to enhance inference speed significantly. At a fine-grained level, we introduce the Multi-Receptive Field Feature Interaction MRFFI module, comprising the Long-Range Wavelet Transform-Enhanced Mamba WTE-Mamba, Efficient Multi-Kernel Depthwise Convolution MK-DeConv, and Eliminate Redundant Identity components. This module integrates multi-receptive field information and enhances high-frequency detail extraction. Additionally, we employ training and testing strategies to further improve performance and efficiency.
MobileMamba achieves up to 83.6% on Top-1, surpassing existing state-of-the-art methods which is maximum x21 faster than LocalVim on GPU. Extensive experiments on high-resolution downstream tasks demonstrate that MobileMamba surpasses current efficient models, achieving an optimal balance between speed and accuracy.

<div align="center">
  <img src="assets/motivation.png" width="800px" />
</div>

> **Top**: Visualization of the *Effective Receptive Fields* (ERF) for different architectures. 
> **Bottom**: Performance *vs.* FLOPs with recent CNN/Transformer/Mamba-based methods.<br>

<div align="center">
  <img src="assets/comparewithmamba.png" width="600px" />
</div>

> ***Accuracy*** *vs.* ***Speed*** with Mamba-based methods.

# Codes
The internal code review is in progress and is expected to be completed within a month, after which the code will be open-sourced.

# Citation
If our work is helpful for your research, please consider citing:
```angular2html
@article{mobilemamba,
  title={MobileMamba: Lightweight Multi-Receptive Visual Mamba Network},
  author={Haoyang He and Jiangning Zhang and Yuxuan Cai and Hongxu Chen and Xiaobin Hu and Zhenye Gan and Yabiao Wang and Chengjie Wang and Yunsheng Wu and Lei Xie},
  journal={arXiv preprint arXiv:2411.15941},
  year={2024}
}
```



