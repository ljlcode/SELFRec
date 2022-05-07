<img src="https://i.ibb.co/54vTYzk/ssl-logo.png" alt="ssl-logo" border="0">

<p float="left"><img src="https://img.shields.io/badge/python-v3.7+-red"> <img src="https://img.shields.io/badge/pytorch-v1.7+-blue"> <img src="https://img.shields.io/badge/tensorflow-v1.14+-green">  <br>

**SELFRec** is a Python framework for self-supervised recommendation (SSR) which integrates commonly used datasets and metrics, and implements many state-of-the-art SSR models. SELFRec has a lightweight architecture and provides user-friendly interfaces. It can facilitate model implementation and evaluation.
<br>
**Founder and principal contributor**: [@Coder-Yu ](https://github.com/Coder-Yu) [@xiaxin1998](https://github.com/xiaxin1998) <br>
**Supported by**: [@AIhongzhi](https://github.com/AIhongzhi) (<a href="https://sites.google.com/view/hongzhi-yin/home">A/Prof. Hongzhi Yin</a>, UQ)

### More models will be released soon...
  
<h2>Architecture<h2>
<img src="https://raw.githubusercontent.com/Coder-Yu/SELFRec/main/selfrec.jpg" alt="ssl-logo" border="0">


<h2>Features</h2>
<ul>
<li><b>Fast execution</b>: SELFRec is developed with Python 3.7+, Tensorflow 1.14+ and Pytorch 1.7+. All models run on GPUs. Particularly, we optimize the time-consuming procedure of item ranking, drastically reducing the ranking time to seconds (less than 10 seconds for the scale of 10,000×50,000). </li>
<li><b>Easy configuration</b>: SELFRec provides a set of simple and high-level interfaces, by which new SSR models can be easily added in a plug-and-play fashion.</li>
<li><b>Highly Modularized</b>: SELFRec is divided into multiple discrete and independent modules/layers. This design decouples the model design from other procedures. For users of SELFRec, they just need to focus on the logic of their method, which streamlines the development.</li>
<li><b>SSR-Specific</b>:  SELFRec is designed for SSR. For the data augmentation and self-supervised tasks, it provides specific modules and interfaces for rapid development.</li>
</ul>

<h2>Requirements</h2>
<ul>
<li>numba==0.53.1</li>
<li>numpy==1.20.3</li>
<li>scipy==1.6.2</li>
<li>tensorflow==1.14.0</li>
<li>torch==1.7.0</li>
</ul>

<h2>Implemented Algorithms</h2>

<table class="table table-hover table-bordered">
  <tr>
		<th>Model</th>
		<th>Paper</th>

   </tr>
     <tr>
    <td scope="row">LightGCN</td>
        <td>He et al. LightGCN: Simplifying and Powering Graph Convolution Network for Recommendation, SIGIR'20.
         </td>
      </tr>
           <tr>
    <td scope="row">SimGCL</td>
        <td>Yu et al. Are Graph Augmentations Necessary? Simple Graph Contrastive Learning for Recommendation, SIGIR'22.
         </td>
      </tr>
     <tr>
    <td scope="row">MHCN</td>
        <td>Yu et al. Self-Supervised Multi-Channel Hypergraph Convolutional Network for Social Recommendation, WWW'21.
         </td>
      </tr>
     <tr>
    <td scope="row">SGL</td>
        <td>Wu et al. Self-supervised Graph Learning for Recommendation, SIGIR'21.
         </td>
      </tr>
    <tr>
    <td scope="row">SEPT</td>
        <td>Yu et al. Socially-Aware Self-supervised Tri-Training for Recommendation, KDD'21.
         </td>
      </tr>
          <tr>
    <td scope="row">BUIR</td>
        <td>Lee et al. Bootstrapping User and Item Representations for One-Class Collaborative Filtering, SIGIR'21.
         </td>
      </tr>
    <tr>
    <td scope="row">SelfCF</td>
        <td>Zhou et al. SelfCF: A Simple Framework for Self-supervised Collaborative Filtering, arXiv'21.
         </td>
      </tr>
  </table>

<h2>Related Datasets</h2>
<div>
 <table class="table table-hover table-bordered">
  <tr>
    <th rowspan="2" scope="col">Data Set</th>
    <th colspan="5" scope="col" class="text-center">Basic Meta</th>
    <th colspan="3" scope="col" class="text-center">User Context</th> 
    </tr>
  <tr>
    <th class="text-center">Users</th>
    <th class="text-center">Items</th>
    <th colspan="2" class="text-center">Ratings (Scale)</th>
    <th class="text-center">Density</th>
    <th class="text-center">Users</th>
    <th colspan="2" class="text-center">Links (Type)</th>
    </tr>   
   <tr>
    <td><a href="https://pan.baidu.com/s/1hrJP6rq" target="_blank"><b>Douban</b></a> [1]</td>
    <td>2,848</td>
    <td>39,586</td>
    <td width="6%">894,887</td>
    <td width="10%">[1, 5]</td>
    <td>0.794%</td>
    <td width="4%">2,848</td>
    <td width="5%">35,770</td>
    <td>Trust</td>
    </tr> 
	 <tr>
    <td><a href="http://files.grouplens.org/datasets/hetrec2011/hetrec2011-lastfm-2k.zip" target="_blank"><b>LastFM</b></a> [2]</td>
    <td>1,892</td>
    <td>17,632</td>
    <td width="6%">92,834</td>
    <td width="10%">implicit</td>
    <td>0.27%</td>
    <td width="4%">1,892</td>
    <td width="5%">25,434</td>
    <td>Trust</td>
    </tr> 
    <tr>
    <td><a href="https://www.dropbox.com/sh/h97ymblxt80txq5/AABfSLXcTu0Beib4r8P5I5sNa?dl=0" target="_blank"><b>Yelp</b></a> [3]</td>
    <td>19,539</td>
    <td>21,266</td>
    <td width="6%">450,884</td>
    <td width="10%">implicit</td>
    <td>0.11%</td>
    <td width="4%">19,539</td>
    <td width="5%">864,157</td>
    <td>Trust</td>
    </tr>
    <tr>
    <td><a href="https://www.dropbox.com/sh/20l0xdjuw0b3lo8/AABBZbRg9hHiN42EHqBSvLpta?dl=0" target="_blank"><b>Amazon-Book</b></a> [4]</td>
    <td>52,463</td>
    <td>91,599</td>
    <td width="6%">2,984,108</td>
    <td width="10%">implicit</td>
    <td>0.11%</td>
    <td width="4%">-</td>
    <td width="5%">-</td>
    <td>-</td>
    </tr>  
  </table>
</div>

<h3>Reference</h3>
<p>[1]. G. Zhao, X. Qian, and X. Xie, “User-service rating prediction by exploring social users’ rating behaviors,” IEEE Transactions on Multimedia, vol. 18, no. 3, pp. 496–506, 2016.</p>
<p>[2]. Iván Cantador, Peter Brusilovsky, and Tsvi Kuflik. 2011. 2nd Workshop on Information Heterogeneity and Fusion in Recom- mender Systems (HetRec 2011). In Proceedings of the 5th ACM conference on Recommender systems (RecSys 2011). ACM, New York, NY, USA</p>
<p>[3]. Yu et al. Self-Supervised Multi-Channel Hypergraph Convolutional Network for Social Recommendation, WWW'21.</p>
<p>[4]. He et al. LightGCN: Simplifying and Powering Graph Convolution Network for Recommendation, SIGIR'20.</p>

<h2>Reference</h2>
If you find this repo helpful to your research, please cite our paper.
  
```
@article{yu2022self,
  title={Self-Supervised Learning for Recommender Systems: A Survey},
  author={Yu, Junliang and Yin, Hongzhi and Xia, Xin and Chen, Tong and Li, Jundong and Huang, Zi},
  journal={arXiv preprint arXiv:2203.15876},
  year={2022}
}
```
