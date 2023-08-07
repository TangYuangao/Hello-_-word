# 这是我撰写的第一篇论文

    这是我的第一篇论文，花费了我很长的时间和精力。在构思这篇文章的过程中，参考小伙伴们在github社区上分享的代码给予了不少灵感。首先对在GitHub上贡献自己代码的小伙伴们表示感谢！为此我也准备将论文部分代码公布出来给大家做一个参考。
    首先是该论文中实验情况的基本介绍，对论文中的实验准备做补充：
    1、mmdetection 2.25.2; mmcv-full 1.7.0
     **注意：** mmdetection 3.x版本进行了一次大更新，部分功能实现方式有所更改，所以如果想对本实验进行复现和测试，建议采用以上版本。
    2、在yolov3上进行实验时，需根据不同数据集使用kmeans算法归类出anchors。
    3、公布的代码是以RetinaNet为基础检测网络，感兴趣的小伙伴可以在其他模型上进行尝试。

## 关于config文件夹
    文件夹中包括了 414*416的Retinanet，RetinaNet+SSRFPN，Retinanet+SSRFPN+CSD三个文件，都是介于DIOR数据集进行设置的，832*832的RetinaNet可自行训练。
## 关于detectors文件夹
    文件夹中包括对新文件中函数的声明及蒸馏网络相关函数，复制到mmdet中detectors文件夹中。
## 关于head文件夹
    包括蒸馏网络的head相关函数，可自行添加声明致__init__.py中。
## 关于neck文件夹
     fpn_ESPCN2.py中是训练好的教师网络，fpn_trainESPCN是针对学生网络进行训练。
