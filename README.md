# DSAN
A PyTorch implementation of 'Deep Subdomain Adaptation Network for Image Classification' which has published on IEEE Transactions on Neural Networks and Learning Systems.
The contributions of this paper are summarized as follows. 
* They propose a novel deep neural network architecture for Subdomain Adaptation, which can extend the ability of deep adaptation networks by capturing the fine-grained information for each category.
* They show that DSAN which is a non-adversarial method can achieve the remarkable results. In addition, their DSAN is very simple and easy to implement.
## Requirement
* python 3
* pytorch 1.0

## Usage
1. You can download Office31 dataset [here](https://pan.baidu.com/s/1o8igXT4#list/path=%2F). And then unrar dataset in ./dataset/.
2. You can change the `src` and `tgt` in `main.py` to set different transfer tasks.
3. Run `python main.py`.

## Results on Office31
| Method | A - W | D - W | W - D | A - D | D - A | W - A | Average |
|:--------------:|:-----:|:-----:|:-----:|:-----:|:----:|:----:|:-------:|
| DSAN | 93.6±0.2 | 98.4±0.1 | 100.0±0.0 | 90.2±0.7 | 73.5±0.5 | 74.8±0.4 | 88.4 |

> Note that for tasks D-A and W-A, setting epochs = 800 or larger could achieve better performance.

## Results on CWRU
| Method | A - D | A - C | B - C | C - A | D - B  |AB-CD|
|:------:|:-----:|:-----:|:----: |:-----:| :-----:|:------:|
| DSAN   |100±0.0|100±0.1|100±0.0|100±0.0|88.88±0.1|100±0.1|
## Reference

```
Zhu Y, Zhuang F, Wang J, et al. Deep Subdomain Adaptation Network for Image Classification[J]. IEEE Transactions on Neural Networks and Learning Systems, 2020.
```

or in bibtex style:

```
@article{zhu2020deep,
  title={Deep Subdomain Adaptation Network for Image Classification},
  author={Zhu, Yongchun and Zhuang, Fuzhen and Wang, Jindong and Ke, Guolin and Chen, Jingwu and Bian, Jiang and Xiong, Hui and He, Qing},
  journal={IEEE Transactions on Neural Networks and Learning Systems},
  year={2020},
  publisher={IEEE}
}
```
```
1. 数据集来源https://github.com/yyxyz/CaseWesternReserveUniversityData
2. 按照任务划分，分为A、B、C、D四个任务按照不同的负载划分也是不同的域，来自论文[基于改进残差网络深度子域适应的变工况下
滚动轴承故障诊断方法]

```