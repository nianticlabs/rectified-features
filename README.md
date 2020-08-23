# [Single-Image Depth Prediction Makes Feature Matching Easier](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123610460.pdf)

**[Carl Toft](https://scholar.google.com/citations?hl=en&user=vvgmWA0AAAAJ&view_op=list_works&sortby=pubdate), [Daniyar Turmukhambetov](http://dantkz.github.io/about), [Torsten Sattler](https://scholar.google.com/citations?user=jzx6_ZIAAAAJ&hl=en), [Fredrik Kahl](http://www.maths.lth.se/matematiklth/personal/fredrik/) and [Gabriel J. Brostow](http://www0.cs.ucl.ac.uk/staff/g.brostow/) – ECCV 2020**


[Link to paper](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123610460.pdf)  
  

<p align="center">
  <a href="https://storage.googleapis.com/niantic-lon-static/research/rectified-features/short-video.mp4">
  <img src="assets/2min.png" alt="2 minute ECCV presentation video link" width="400">
  </a>
</p>


<p align="center">
  <a href="https://storage.googleapis.com/niantic-lon-static/research/rectified-features/long-video.mp4">
  <img src="assets/10min.png" alt="10 minute ECCV presentation video link" width="400">
  </a>
</p>


**Supplementary pdf and dataset are coming soon...**  


Good local features improve the robustness of many 3D relocalization and multi-view reconstruction pipelines. The problem is that viewing angle and distance severely impact the recognizability of a local feature. Attempts to improve appearance invariance by choosing better local feature points or by leveraging outside information, have come with pre-requisites that made some of them impractical. In this paper, we propose a surprisingly effective enhancement to local feature extraction, which improves matching.

<p align="center">
  <img src="assets/teaser.png" alt="We use single-image depth estimation to account for perspective distortion when extracting local features" width="600" />
</p>

We show that CNN-based depths inferred from single RGB images are quite helpful, despite their flaws. They allow us to pre-warp images and rectify perspective distortions, to significantly enhance SIFT and BRISK features, enabling more good matches, even when cameras are looking at the same scene but in opposite directions.

<p align="center">
  <img src="assets/pipeline.png" alt="Our pipeline" width="600" />
</p>

Our pipeline finds planar patches according to estimated depth, and extracts features from rectified views of these patches. Non-rectified features are also extracted from regions that do not belong to planar patches.

## ✏️ 📄 Citation

If you find our work useful or interesting, please consider citing [our paper](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123610460.pdf):

```
@inproceedings{toft-2020-rectified-features,
 title   = {Single-Image Depth Prediction Makes Feature Matching Easier},
 author  = {Carl Toft and
            Daniyar Turmukhambetov and
            Torsten Sattler and
            Fredrik Kahl and
            Gabriel J. Brostow
           },
 booktitle = {European Conference on Computer Vision ({ECCV})},
 year = {2020}
}
```


# 👩‍⚖️ License
Copyright © Niantic, Inc. 2020. Patent Pending. All rights reserved. Please see the license file for terms.
