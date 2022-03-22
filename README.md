# NWPU_YRCC_EX
A dataset for ice segmentation
## Overview
The Yellow River is the main birthplace of Chinese civilization. The Yellow River spans a large latitude range, and ice flood is easy to occur in the upstream and downstream (Ningxia, Inner Mongolia, Shanxi, Shaanxi and Shandong). From 1987 to 2015, there were 67 ice flood disasters. The management and governance of the Yellow River involves many fields, such as flood control and disaster relief, water conservancy management, soil and water conservation, embankment safety and disease prevention, water conservancy informatization and so on. Therefore, the prevention of the Yellow River disaster is very important.
### Paper Link
The paper can be downloaded from this [link](https://www.researchgate.net/publication/338489960_ICENET_A_Semantic_Segmentation_Deep_Network_for_River_Ice_by_Fusing_Positional_and_Channel-Wise_Attentive_Features). 
Please cite our paper when using the dataset.
```
@article{zhang2020icenet,
  title={ICENET: A semantic segmentation deep network for river ice by fusing positional and channel-wise attentive features},
  author={Zhang, Xiuwei and Jin, Jiaojiao and Lan, Zeze and Li, Chunjiang and Fan, Minhao and Wang, Yafei and Yu, Xin and Zhang, Yanning},
  journal={Remote Sensing},
  volume={12},
  number={2},
  pages={221},
  year={2020},
  publisher={Multidisciplinary Digital Publishing Institute}
}
```
## Dataset Details
We selected the Ningxia–Inner Mongolia reach of the Yellow River as our study area. It spans 23 longitudes from east to west and 10 latitudes from north to south, hence there are considerable differences in elevation between the east and west, and in landforms among different regions. Due to the complexity of climate and landform, the ice phenomenon is very typical and diverse in spring and winter, especially in the Ningxia–Inner Mongolia reach. Therefore, this reach is selected so as to study river ice segmentation.

To the best of our knowledge, there is no public UAV image dataset for river ice monitoring. To promote the study of river ice monitoring based on deep learning, a UAV visible image dataset was built for river ice segmentation. As mentioned in the first section, the ice on the Yellow River, especially in the Ningxia–Inner Mongolia reach, is very typical and diverse. Therefore, the Yellow River was selected to study the river ice segmentation. To build this dataset, four institutions devoted their efforts, including Northwestern Polytechnical University, the Yellow River Institute of Hydraulic Research, the Hydrology Bureau of the Yellow River Conservancy Commission and the Ningxia–Inner Mongolia Hydrology Bureau. The latter three are the subordinates of the Yellow River Conservancy Commission. Thus, it was named the NWPU_YRCC river ice dataset, short for the Northwestern Polytechnical University/Yellow River Conservancy Commission dataset.

The appearance of river ice varies a lot at different times; in order to cover different periods of river ice, we took a lot of aerial videos during November–March over four years. A total of 814 typical frames were carefully selected from these video sequences to form the dataset. All frames in this dataset were accurately annotated pixel by pixel by three classification labels, ice, water and shore. The details of this dataset are in the following two subsections.
### Dataset Construction
