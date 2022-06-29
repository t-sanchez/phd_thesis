# Learning to sample in Cartesian MRI
This repository contains the source file of my PhD thesis, entitled **Learning to sample in Cartesian MRI**, and supervised by Volkan Cevher. This was completed at EPFL between 2018 and 2022. The published version of my thesis is available on [infoscience](https://infoscience.epfl.ch/record/294077?ln=en).

Please cite it using the following BibTeX entry: 
```
@article{sanchez2022learning,
      title = {Learning to sample in Cartesian MRI},
      author = {Sanchez, Thomas},
      institution = {IEM},
      publisher = {EPFL},
      address = {Lausanne},
      pages = {192},
      year = {2022},
      url = {http://infoscience.epfl.ch/record/294077},
      doi = {10.5075/epfl-thesis-9981},
}
```
The repository also contains the slides used in my private defense and public defense (done in French).
## About the thesis

### Abstract
Magnetic Resonance Imaging (MRI) is a non-invasive, non-ionizing imaging modality with unmatched soft tissue contrast. However, compared to imaging methods like X-ray radiography, MRI suffers from long scanning times, due to its inherently sequential acquisition procedure. Shortening scanning times is crucial in clinical setting, as it increases patient comfort, decreases examination costs and improves throughput.
Recent developments thanks to compressed sensing (CS) and lately deep learning allow to reconstruct high quality images from undersampled images, and have the potential to greatly accelerate MRI. Many algorithms have been proposed in the context of recon- struction, but comparatively little work has been done to find acquisition trajectories that optimize the quality of the reconstructed image downstream.

Although in recent years, this problem has gained attention, it is still unclear what is the best approach to design acquisition trajectories in Cartesian MRI. In this thesis, we aim at contributing to this problem along two complementary directions.

First, we provide novel methodological contributions to this problem. We first propose two algorithms that improve drastically the greedy learning-based compressed sensing (LBCS) approach of Gözcü et al. (2018). These two algorithms, called lazy LBCS and stochastic LBCS scale to large, clinically relevant problems such as multi-coil 3D MR and dynamic MRI that were inaccessible to LBCS. We also show that generative adversarial networks (GANs), used to model the posterior distribution in inverse problems, provide a natural criterion for adaptive sampling by leveraging their variance in the measurement
domain to guide the acquisition procedure.

Secondly, we aim at deepening the understanding of the kind of structures or assumptions that enable mask design algorithms to perform well in practice. In particular, our experiments show that state-of-the-art approaches based on deep reinforcement learning (RL), which have the ability to adapt trajectories on the fly to patient and perform long-horizon planning, bring at best a marginal improvement over stochastic LBCS, which is neither adaptive nor does long-term planning.

Overall, our results suggest that methods like stochastic LBCS offer promising alternatives to deep RL. They shine in particular by their scalability and computational efficiency and could be key in the deployment of optimized acquisition trajectories in Cartesian MRI.

### Organization of the thesis
1. Introduction
2. MRI Background
3. Reconstruction methods
4. Optimizing sampling patterns
5. Scalable learning-based sampling optimization
6. On the benefits of deep RL in accelerated MRI sampling
7. Uncertainty driven adaptive sampling via GANs 
8. Conclusion and future works 
A. Appendix for Chapter 6 
B. Appendix for Chapter 7 
C. Bibliography 
D. Curriculum Vitae

## Organization of the repository
The repository contains 4 main folders.

- `figures`: contains the figures used in the manuscripts as well as presentation.
- `phd_thesis`: contains the source file of the PhD manuscript (`thesis.tex`). The compiled version is freely available on [infoscience](https://infoscience.epfl.ch/record/294077/files/EPFL_TH9981.pdf?ln=en).
- `private_defense`: contains the source file of the slides used in the private defense (`thesis_presentation.tex`), as well as the compiled version (`thesis_presentation.pdf`).
- `public defense`: contains the pdf exported version of the slides used in the public defense originally done in Keynote.

## Building the files 
Building was done from command line and was tested on both MacOS (Monterey) as well as Ubuntu 22.04, using a standard LaTeX installation on these systems. To build, call from their respective folders (i.e. from `phd_thesis` or `private_defense`)

```
latexmk -pdf thesis.tex/thesis_presentation.tex
```

## About the repository
The repo uses git large file system, check that it is installed on your machine. If not, you can install it (check [this link](https://git-lfs.github.com/), and if you already clone the repository, you will need to initalize it in locally using `git lfs install`. You can then obtain the large files with `git lfs pull`.

## Source
This thesis is based of the [unofficial EPFL thesis template](https://github.com/glederrey/EPFL_thesis_template).

