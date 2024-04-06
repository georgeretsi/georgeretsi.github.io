---
layout: publication
title: "SMIRK: 3D Facial Expressions through Analysis-by-Neural-Synthesis (CVPR 2024)"
description: # "SMIRK: 3D Facial Expressions through Analysis-by-Neural-Synthesis (CVPR 2024)"
img: assets/img/cover.jpg
importance: 1
category: work
---
<style type="text/css">
  .post-title {
    text-align: center;
    font-family: "Google Sans", sans-serif;
    /* color: #363636; */
    font-size: 2rem;
    font-weight: 400;
    line-height: 1.125;
  }
  .publication-authors
  {
    margin-top: 15px;
    text-align: center;
    font-family: "Google Sans", sans-serif;
  }
  h3 {
    font-family: "Google Sans", sans-serif;
    /* color: #363636; */
    font-weight: 400;
    line-height: 1.125;
    text-align: center;
    margin-top: 30px;
    margin-bottom: 30px;
  }
  .btn {
    /*color: white;*/
    padding: .5rem 1.5rem;
    text-transform: none;
    font-size: 17px;
  }
  .btn span {
    /*color:white;*/
  }

  .btn:hover {
    text-decoration: underline;
  }

  .btn.btn-youtube {
    /*background: #FF3636 !important;*/
  }

  .publication-icons {
    margin-top: 30px;
    margin-bottom: 30px;
  }

  .abstract {
    text-align: justify;
  }

</style>

<div class="publication-authors">
  <span class="author-block">
    <a href="https://georgeretsi.github.io">George Retsinas</a><sup>*</sup>,
  </span>
  <span class="author-block">
    <a href="https://filby89.github.io">Panagiotis P. Filntisis</a><sup>*</sup>,
 </span>
  <span class="author-block">
    <a href="https://ps.is.mpg.de/person/rdanecek">Radek Daněček</a>,
  </span>
  <span class="author-block">
    <a href="https://is.mpg.de/~vabrevaya">Victoria F. Abrevaya</a>,
  </span>
  <span class="author-block">
    <a href="https://users.ics.forth.gr/~troussos/">Anastassios Roussos</a>,
  </span>
  <span class="author-block">
    <a href="https://sites.google.com/site/bolkartt/">Timo Bolkart</a>,
  </span>
  <span class="author-block">
    <a href="https://robotics.ntua.gr/members/maragos/">Petros Maragos</a>
  </span>
</div>

<div class="row publication-icons">
  <div class="col-sm" align=center>
        <!-- PDF Link. -->
        <!-- Video Link. -->
        <a class="btn btn-dark btn-rounded" href="https://arxiv.org/pdf/2207.11094" role="button">
          <i class="fa fa-file-pdf"></i>
          Paper
        </a>
        <a class="btn btn-dark" href="https://arxiv.org/abs/2207.11094" role="button">
          <i class="ai ai-arxiv"></i>
          arXiv
        </a>
        <!-- Video Link. -->
        <a class="btn btn-dark btn-youtube" style="background-color: #ed302f; !important" href="https://youtu.be/8ZVgr41wxbk" role="button">
          <i class="fab fa-youtube"></i>
          Video
        </a>
        <!-- Code Link. -->
        <!-- Github -->
        <a class="btn btn-dark" href="https://github.com/georgeretsi/smirk" role="button">
          <i class="fab fa-github"></i>
          Code
        </a>
  </div>
</div>

<!-- <div class="alert alert-info">
<b>tl;dr:</b> we improve 3D facial reconstruction in videos by focusing on the lip formations and mouth movements, using a <b>lipreading</b> loss
</div> -->

<div class="row">
    <div class="col-sm">
        {% include figure.html path="assets/img/cover.jpg" title="Cover image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    SMIRK reconstructs 3D faces from monocular images with facial geometry that faithfully recover extreme, asymmetric, and subtle expressions.
</div>


<div class="row">
  <div class="col-sm">
    <h3>Teaser Video</h3>
  </div>
</div>

<div class="row justify-content-sm-center" align="center">
    <div class="col-sm">
<iframe width="560" height="315" src="https://youtu.be/8ZVgr41wxbk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
</div>




<div class="row">
  <div class="col-sm">
    <h3>Abstract</h3>
  </div>
</div>

<p class="abstract">
While existing methods for 3D face reconstruction from in-the-wild images excel at recovering the overall face shape, they commonly miss subtle, extreme, asymmetric, or rarely observed expressions. We improve upon these methods with  SMIRK (Spatial Modeling for Image-based Reconstruction of Kinesics), which faithfully reconstructs expressive 3D faces from images. We identify two key limitations in existing methods: shortcomings in their self-supervised training formulation, and a lack of expression diversity in the training images. For training, most methods employ differentiable rendering to compare a predicted face mesh with the input image, along with a plethora of additional loss functions. This differentiable rendering loss not only has to provide supervision to optimize for 3D face geometry, camera, albedo, and lighting, which is an ill-posed optimization problem, but the domain gap between rendering and input image further hinders the learning process. Instead, SMIRK replaces the differentiable rendering with a neural rendering module that, given the rendered predicted mesh geometry, and sparsely sampled pixels of the input image, generates a face image. As the neural rendering gets color information from sampled image pixels, supervising with neural rendering-based reconstruction loss can focus solely on the geometry. Further, it enables us to generate images of the input identity with varying expressions while training. These are then utilized as input to the reconstruction model and used as supervision with ground truth geometry. This effectively augments the training data and enhances the generalization for diverse expressions. Our qualitative, quantitative and particularly our perceptual evaluations demonstrate that SMIRK achieves the new state-of-the art performance on accurate expression reconstruction. For our method's source code, demo video and more, please visit our project webpage: <a href="https://georgeretsi.github.io/smirk/">https://georgeretsi.github.io/smirk/</a>.
</p>


<!-- <h3> Bibtex </h3> -->

<div class="publications">
{% bibliography --template bibtex_only -q @*[key=filntisis2022visual]* %}
</div>