---
layout: page
title: Academic Works
permalink: /works/
last_updated: 2023-04-25
---

This page contains a list of my publications and other projects I have done. **_To see my curriculum vitae/resume, see <a href="/cv/cv.pdf">here</a>._**

<!-- For a list of some classes I have taken in my undergraduate (with rough descriptions of the classes), see <a href="courses_taken.pdf">this document</a>. -->

<br> 

# Publications

<small>
Note: asterisks* denotes equal contributions.
</small>

<ol class="listing">

<li class="listing-item">

PIED: Physics-Informed Experimental Design For Inverse Problems.
<br>
<b>Apivich Hemachandra*</b>, Gregory Kang Ruey Lau*, See-Kiong Ng and Bryan Kian Hsiang Low.
<br>
<i>ICML 2024 AI4Science Workshop.</i> 
<br>

<details> 
<summary>
<a class="color-button">abstract (click to show)</a>
</summary>
<small>
In many inverse problems (IPs) in science and engineering, optimization of design parameters (e.g., sensor placement) with experimental design (ED) methods is performed due to high data acquisition costs when conducting physical experiments, and often has to be done up front due to practical constraints on sensor deployments. However, existing ED methods are often challenging to use in practical PDE-based inverse problems due to significant computational bottlenecks during forward simulation and inverse parameter estimation. This paper presents Physics-Informed Experimental Design (PIED), the first ED framework that makes use of PINNs in a fully differentiable architecture to perform continuous optimization of design parameters for IPs. PIED utilizes techniques such as learning of a shared NN parameter initialization, and approximation of PINN training dynamics during the ED process, for better estimation of the inverse parameters. PIED selects the optimal design parameters for one-shot deployment, allows exploitation of parallel computation unlike existing methods, and is empirically shown to significantly outperform existing ED benchmarks in IPs for both finite-dimensional and function-valued inverse parameters given limited budget for observations.
</small>
</details>

</li>
<br>
<li class="listing-item">

PINNACLE: PINN Adaptive ColLocation and Experimental points selection.
<br>
Gregory Kang Ruey Lau*, <b>Apivich Hemachandra*</b>, See-Kiong Ng and Bryan Kian Hsiang Low.
<br>
<i>ICLR 2024 Spotlight Presentation.</i> Acceptance rate: 5%.
<br>
<i>Also received Best Paper Award at ICML 2024 AI4Science Workshop.</i> 
<br>

<details> 
<summary>
<a class="color-button">abstract (click to show)</a>
<a class="color-button" href="/docs/paper/iclr24.pdf">pdf</a>
<a class="color-button" href="/docs/poster/iclr24.pdf">poster</a>
<a class="color-button" href="https://arxiv.org/abs/2404.07662">arXiv</a>
<a class="color-button" href="https://github.com/apivich-h/pinnacle">code (GitHub)</a>
</summary>
<small>
Physics-Informed Neural Networks (PINNs), which incorporate PDEs as soft constraints, train with a composite loss function that contains multiple training point types: different types of collocation points chosen during training to enforce each PDE and initial/boundary conditions, and experimental points which are usually costly to obtain via experiments or simulations. Training PINNs using this loss function is challenging as it typically requires selecting large numbers of points of different types, each with different training dynamics. Unlike past works that focused on the selection of either collocation or experimental points, this work introduces PINN Adaptive ColLocation and Experimental points selection (PINNACLE), the first algorithm that jointly optimizes the selection of all training point types, while automatically adjusting the proportion of collocation point types as training progresses. PINNACLE uses information on the interactions among training point types, which had not been considered before, based on an analysis of PINN training dynamics via the Neural Tangent Kernel (NTK). We theoretically show that the criterion used by PINNACLE is related to the PINN generalization error, and empirically demonstrate that PINNACLE is able to outperform existing point selection methods for forward, inverse, and transfer learning problems.
</small>
</details>

</li>
<br>
<li class="listing-item">

Training-Free Neural Active Learning With Initialization-Robustness Guarantees.
<br>
<b>Apivich Hemachandra</b>, Zhongxiang Dai, Jasraj Singh, See-Kiong Ng and Bryan Kian Hsiang Low.
<br>
<i>ICML 2023.</i> Acceptance rate: 27.9%.
<br>

<details> 
<summary>
<a class="color-button">abstract (click to show)</a>
<a class="color-button" href="/docs/paper/icml23.pdf">pdf</a>
<a class="color-button" href="/docs/poster/icml23.pdf">poster</a>
<a class="color-button" href="http://arxiv.org/abs/2306.04454">arXiv</a>
<a class="color-button" href="https://github.com/apivich-h/init-robust-al">code (GitHub)</a>
</summary>
<small>
Existing neural active learning algorithms have aimed to optimize the predictive performance of neural networks (NNs) by selecting data for labelling.
However, other than a good predictive performance, being robust against random parameter initializations is also a crucial requirement in safety-critical applications.
To this end, we introduce our <i>expected variance with Gaussian processes</i> (EV-GP) criterion for neural active learning, which is theoretically guaranteed to select data points which lead to trained NNs with both (a) good predictive performances and (b) initialization robustness.
Importantly, our EV-GP criterion is training-free, i.e., it does not require any training of the NN during data selection, which makes it computationally efficient.
We empirically demonstrate that our EV-GP criterion is highly correlated with both initialization robustness and generalization performance, and show that it consistently outperforms baseline methods in terms of both desiderata, especially in situations with limited initial data or large batch sizes.
</small>
</details>

</li>

</ol>

<br>

# Undergraduate Senior Thesis

The title of my undergraduate thesis is **"Data Diversification in Different Domains"**. You can visit <a href="/projects/thesis-u">this page</a> for further details.

<br>

# Industry-Related Projects

I, with a few others, are working on projects with PTTEP, a Thai company who deals with extraction of petroleum. The projects I work on involves automation of tasks currently done by human, and will often require skills and knowledge from machine learning, statistics, mathematics and even physics. 
<!-- To make sure I do not break any non-disclosure agreements, I will not be describing the details of the projects here. -->

<br>

# Other Projects

For other projects I have done in the past (mostly pre-2020 during my undergraduate), see <a href="/projects-old">here</a>.
