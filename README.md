# VGMMamba
Abstract: Low-light image enhancement is a fundamental task in computer vision. Recently, Mamba-based architectures have attracted increasing attention due to
their superior capability in modeling long-range dependencies and linear computational complexity. However, existing methods still suffer from insufficient
feature extraction and loss of visual information in practical applications. To
address the limited feature representation during enhancement, we propose a
Vision Guide Module (VGM) that introduces auxiliary visual cues throughout the enhancement process, enabling more effective restoration of image
details. To mitigate the “long-range forgetting” issue caused by the sequential scanning mechanism of Mamba, we design a Global-Local Feature Enhancement (GLFE) module, which strengthens long-range feature modeling
through a global-local feature refinement strategy. Moreover, conventional
models typically focus on spatial-domain feature extraction while neglecting
channel-wise information, leading to incomplete feature representation. To
tackle this limitation, we introduce a Multidimensional Feature Feed-Forward
Module (MFFM) that jointly captures and fuses features across both spatial
and channel dimensions, thereby improving the overall enhancement performance. Extensive experiments are conducted on multiple datasets using
various evaluation metrics. Under the supervised LoLv2-real dataset, ourmethod achieves improvements of 0.41 dB in PSNR and 0.009 in SSIM; on
LoLv2-syn, it gains 0.161 dB in PSNR and 0.004 in SSIM. On the unsupervised LIME dataset, the NIQE and PI scores are reduced by 0.202 and
0.142, respectively, indicating better perceptual quality.

# Network Architecture
![VGMMamba](https://github.com/user-attachments/assets/bc752afd-8600-45cf-b27f-3701d3c2b6d6)

#   Environment
        conda create -n VGMMamba python=3.8
        conda activate VGMMamba
        pip install torch==1.13.0 torchvision==0.14.0 torchaudio==0.13.0 --extra-index-url https://download.pytorch.org/whl/cu117
        pip install packaging
        pip install timm==0.4.12
        pip install pytest chardet yacs termcolor
        pip install submitit tensorboardX
        pip install triton==2.0.0
        pip install causal_conv1d==1.0.0  # causal_conv1d-1.0.0+cu118torch1.13cxx11abiFALSE-cp38-cp38-linux_x86_64.whl
        pip install mamba_ssm==1.0.1  # mmamba_ssm-1.0.1+cu118torch1.13cxx11abiFALSE-cp38-cp38-linux_x86_64.whl
        pip install scikit-learn matplotlib thop h5py SimpleITK scikit-image medpy yacs opencv-python tensorboard

#  Training
    python trian.py

#  Testing
    python test.py -opt tasks/***.yml
    Example:
    python test.py -opt Enhancement/LoLv2_real.yml
    
