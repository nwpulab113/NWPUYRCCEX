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

To the best of our knowledge, there is no public UAV image dataset for river ice monitoring. To promote the study of river ice monitoring based on deep learning, a UAV visible image dataset was built for river ice segmentation. As mentioned before, the ice on the Yellow River, especially in the Ningxia–Inner Mongolia reach, is very typical and diverse. Therefore, the Yellow River was selected to study the river ice segmentation. To build this dataset, four institutions devoted their efforts, including Northwestern Polytechnical University, the Yellow River Institute of Hydraulic Research, the Hydrology Bureau of the Yellow River Conservancy Commission and the Ningxia–Inner Mongolia Hydrology Bureau. The latter three are the subordinates of the Yellow River Conservancy Commission. Thus, it was named the NWPU_YRCC river ice dataset, short for the Northwestern Polytechnical University/Yellow River Conservancy Commission dataset.

The appearance of river ice varies a lot at different times; in order to cover different periods of river ice, we took a lot of aerial videos during November–March over four years. A total of 814 typical frames were carefully selected from these video sequences to form the NWPU_YRCC. All frames in this dataset were accurately annotated pixel by pixel by three classification labels, ice, water and shore. And we extend the NWPU_YRCC dataset to NWPU_YRCC_EX in 2021. The details of this dataset are in the following two subsections.
### Dataset Construction
#### Collection
The aerial images were captured at the Ningxia–Inner Mongolia reach of the Yellow RiverduringNovember–Marchofeachyearfrom2015to2019. Inordertoobtainanintuitiveview and understanding of environments around image acquisition areas, we exhibit a map in Figure 1, in which the red ellipse reveals our study and imaging area. During the data collection, we used two different UAVs, a fixed wing UAV ASN216 with a Canon 5DS visible light camera and a DJI Inspire 1. The flight height of UAVs ranged from 30 to 500 m. There are 200 videos in total, ranging in length from 10 min to 50 min.
#### Manual Annotation
There are several annotation tools for semantic segmentation, such as Labelme, Image Labeler and so on. However, due to the irregularity of river ice, it is hard to mark a clear boundary between water and ice on the NWPU_YRCC dataset with these tools. Eventually, Photoshop software was adopted to label each pixel in the image as one of three categories, including ice, water and shore. However, there continued to be some problems. Other than three demanding kinds of pixel values, there were still other values in the annotation map. So the unexpected values were classified into three expected kinds using the least Euclidean distance metric. Some very small misclassified regions with only several pixels still existed. To ensure the integrity, an open morphology operation was carried out to correct them. This annotation job is very time-consuming. Finally, 814 typical images were carefully selected to be accurately annotated, and make up the NWPU_YRCC dataset. Note that the resolution of all annotated images is 1600 × 640. However, the resolutions of the collected images are diverse. The maximum image resolution and video resolution of Canon 5DS on ASN216 are, respectively, 8688 × 5792 and 1920 × 1080, while the max image resolution and video resolution of camera on DJI Inspire 1 are 4000 × 3000 and 4096 × 2160. To ensure that the resolution of the input images in the deep convolution neural network was consistent, we finally cropped and resized the images to 1600 × 640. 
#### Extend
Due to the large amount of data required for neural network training, we expanded the NWPU_YRCC data set, added 74 images on the original dateset, and renamed it as NWPU_YRCC_EX. There are 887 images in the NWPU_YRCC_EX dataset. At the same time, we re divided the dataset according to the ice shape, texture and other information, including 524 as training sets, 180 as val sets and 183 as test sets. We will continue to expand this data set in the future.
## Data Orgnization
     -Dataset
      -train
      -trainannot
      -val
      -valannot
      -test
      -testannot
