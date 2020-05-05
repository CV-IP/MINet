# Multi-scale Interactive Network for Salient Object Detection

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

CVPR 2020.

## Changelog

The code and experimental results have be released now :smile:.

* 2020/5/6: Add some new attempts and improvements.
    *  Modified the method of importing model from the directly setting in config.py, and change it to the automatic selection and instantiation of the specific model class according to the model alias (`exp_name` in config.py).
    * Added a lighter setting for AIM and MInet.
    * Added an attempt to `checkpoint` features of PyTorch.
    * Added learning rate decay strategy with learning rate warm-up. However, the parameter setting is not flexible at present, and needs to be improved.
    * A new optimization strategy has been added to imitate the settings from F3Net.
* 2020/4/16: Modify some misleading descriptions in the `readme.md` file.
* 2020/4/7: Simplify the structure of the repository.
* 2020/3/29: Update the method of evaluating results. (See the [`readme.md`](./code/readme.md#Evaluation) for more details.)
* 2020/3/28: Update our code, results, pretrained parameters and some documents.

## Repository Details

* `code`: Complete training and testing code about our method. The `readme.md` file describes how to use the code.
* `docs`: Github page about out paper. Here are some paper details.

## Related Links

* Paper:
    - Baidu Pan: <https://pan.baidu.com/s/1zN7m4aeDhRvTOeF2naATRg> (baidu: 48au)
    - Google Drive: <https://drive.google.com/file/d/1gUYu0hO_8Xc5jgpzetuOVFDrqeSOiKZN/view?usp=sharing>
* Results & Pretrained Parameters:
    - https://drive.google.com/drive/folders/16yTcf_m-ehnhWgXlN6hbZpBKMy6lYIQQ?usp=sharing

## Paper Details

### Abstract

> Deep-learning based salient object detection methods achieve great progress. However, the variable scale and unknown category of salient objects are great challenges all the time. These are closely related to the utilization of multi-level and multi-scale features. In this paper, we propose the aggregate interaction modules to integrate the features from adjacent levels, in which less noise is introduced because of only using small up-/down-sampling rates. To obtain more efficient multi-scale features from the integrated features, the self-interaction modules are embedded in each decoder unit. Besides, the class imbalance issue caused by the scale variation weakens the effect of the binary cross entropy loss and results in the spatial inconsistency of the predictions. Therefore, we exploit the consistency-enhanced loss to highlight the fore-/back-ground difference and preserve the intra-class consistency. Experimental results on five benchmark datasets demonstrate that the proposed method without any post-processing performs favorably against 23 state-of-the-art approaches. The source code will be publicly available at https://github.com/lartpang/MINet.

### Architecture

![](./assets/Network.png)

![](./assets/AIM.png)

![](./assets/SIM.png)

### Comparison

![](./assets/TableofResults.png)

![](./assets/CurveFigure.png)

![](./assets/VisualFigure.png)

## BibTeX

```text
@inproceedings{MINet-CVPR2020,
    author = {Youwei Pang and Xiaoqi Zhao and Lihe Zhang and Huchuan Lu},
    title = {Multi-scale Interactive Network for Salient Object Detection},
    booktitle = CVPR,
    year = {2020}
}
```
