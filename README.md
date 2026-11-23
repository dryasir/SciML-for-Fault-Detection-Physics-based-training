# Scientific machine learning for seismic fault and discontinuity detection: physics-based training versus conventional deep learning

# What is this repository for?
Supervised convolutional neural networks (CNNs) are a standard tool for seismic fault interpretation, but depend on manually interpreted labels that are scarce, incomplete, and subjective. We present a scientific machine learning (SciML) approach in which a U-Net learns Faults/discontinuity from physics-based synthetic seismic data: layered impedance models are folded, faulted, and convolved with wavelets matched to the measured spectrum of the target survey, so every training sample carries an exact label, including examples without faults. The network is trained with a class-weighted cross-entropy and Dice loss, masked where labels are unknown, and Monte-Carlo dropout provides predictive uncertainty. We compare the developed method with a conventional CNN trained on five hand-interpreted inlines, as in our earlier study. Because the F3 block (Dutch North Sea) has no complete fault interpretation, both methods are first scored on a benchmark survey with exact ground truth that carries the statistical F3 wavelet and F3-coloured noise. On 18 held-out inlines, SciML fine-tuned on the same five inlines improves F1 from 0.850 to 0.881, IoU from 0.739 to 0.787, and average precision from 0.924 to 0.952, and reduces false alarms by 32% (95% bootstrap interval of the F1 gain: +0.027 to +0.035). Without any survey labels, SciML reaches 97% of the conventional F1 while producing 36% fewer false alarms. On real F3 data, 19.5% of the conventional detections run parallel to reflectors, a signature of false picks on strong horizons, compared with 2.7% for SciML.

# Source Code

1. SciML_vs_Conventional.ipynb

This Jupyter Notebook contains the complete source code for the study, covering the developed methodology from initial data loading and model training, validation, evaluation, and visualization.


# Contact

We welcome feedback, questions, suggestions, and discussions related to the use and further development of this repository. If you use this code in your research or have ideas for improving the workflow, please feel free to contact the author.

Author and Technical Contact:
# _Dr. Yasir Bashir_
Department of Geophysics
Istanbul Technical University (ITU), Türkiye
Email: ybashir@itu.edu.tr, dryasir.bashir@live.com

For questions related to the SciML algorithm, implementation, or reproducibility of the results presented in the paper, please contact Dr. Yasir Bashir.
