# VGMMamba

Low-light image enhancement is a fundamental task in computer vision. Recently, Mamba-based architectures have attracted increasing attention due to
their superior capability in modeling long-range dependencies and linear computational complexity. However, existing methods still suffer from insufficient
feature extraction and loss of visual information in practical applications. To
address the limited feature representation during enhancement, we propose a
Vision Guide Module (VGM) that introduces auxiliary visual cues throughout the enhancement process, enabling more effective restoration of image
details. To mitigate the “long-range forgetting” issue caused by the sequential scanning mechanism of Mamba, we design a Global-Local Feature Enhancement (GLFE) module, which strengthens long-range feature modeling
through a global-local feature refinement strategy. Moreover, conventional
models typically focus on spatial-domain feature extraction while neglecting
channel-wise information, leading to incomplete feature representation. To
tackle this limitation, we introduce a Multidimensional Feature Feed-Forward
Module (MFFM) that jointly captures and fuses features across both spatial
and channel dimensions, thereby improving the overall enhancement performance. Extensive experiments are conducted on multiple datasets using
various evaluation metrics. Under the supervised LoLv2-real dataset, ourmethod achieves improvements of 0.41 dB in PSNR and 0.009 in SSIM; on
LoLv2-syn, it gains 0.161 dB in PSNR and 0.004 in SSIM. On the unsupervised LIME dataset, the NIQE and PI scores are reduced by 0.202 and
0.142, respectively, indicating better perceptual quality.
