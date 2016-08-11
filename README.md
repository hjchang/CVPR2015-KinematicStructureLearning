This directory contains a set of codes for kinematic structure learning develeped at the Personal Robotics Laboratory in Imperial College London, UK. This module is mainly developed in Matlab with OpenCV. 

## Requirements

In order to run the module properly, it is required to install the followings:
- Matlab
- OpenCV 2.3.x
- YARP

Then, the OpenCV and YARP should be connected to Matlab.

1. Matlab + OpenCV
You can use 'mexopencv' for this. 
Here is a well-described manual for the mexopencv setting:
http://vision.is.tohoku.ac.jp/~kyamagu/software/mexopencv/

2. Matlab + YARP
Here are instructions for calling YARP from Matlab:
http://wiki.icub.org/wiki/Calling_yarp_from_Matlab

## How to run the module

1. Loading input data from 'Cam/Video/Images'

	a) Run the 'main_solely.m' code
	
	b) Select a input source by the number. (Note: The '2:Yarp' is not working)
	
	c) Select a video or a folder of images.

2. Loading input data from 'YARP/ABM'

	a) Run the ABM server
	
	b) Check the yarp namespace for ABM

	c) Run the 'main_YARP_trigger.m' code
	
	d) $ yarp rpc /matlab/kinematicStructure/rpc
	
	e) $ startStructureLearning #num_instance [left or right camera] [first frame] [last frame]
	
	f) Closeing module: $ quit 

## Abstract

In this paper we present a novel framework for unsupervised kinematic structure learning of complex articulated objects from a single-view image sequence. In contrast to prior motion information based methods, which estimate relatively simple articulations, our method can generate arbitrarily complex kinematic structures with skeletal topology by a successive iterative merge process. The iterative merge process is guided by a skeleton distance function which is generated from a novel object boundary generation method from sparse points. Our main contributions can be summarised as follows: (i) Unsupervised complex articulated kinematic structure learning by combining motion and skeleton information. (ii) Iterative fine-to-coarse merging strategy for adaptive motion segmentation and structure smoothing. (iii) Skeleton estimation from sparse feature points. (iv) A new highly articulated object dataset containing multi-stage complexity with ground truth. Our experiments show that the proposed method out-performs state-of-the-art methods both quantitatively and qualitatively.

## Publication

[Our paper](http://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Chang_Unsupervised_Learning_of_2015_CVPR_paper.pdf) is open published thanks to the Computer Science Foundation. 

Please cite with the following Bibtex code:

````
@inproceedings{ChangCVPR2015KinematicStructure,
	author = {Hyung Jin Chang and Yiannis Demiris},
	title = {Unsupervised Learning of Complex Articulated Kinematic Structures
	combining Motion and Skeleton Information},
	booktitle = {The IEEE Conference on Computer Vision and Pattern Recognition (CVPR)},
	month = {June},
	year = {2015}
}
```

You may also want to refer to our publication with the more human-friendly Chicago style:

*Hyung Jin Chang and Yiannis Demiris, "Unsupervised learning of complex articulated kinematic structures combining motion and skeleton information," in IEEE Conference on Computer Vision and Pattern Recognition (CVPR), June 2015, pp. 3138–3146.*


## Contact

If you have any general doubt about our work or code which may be of interest for other researchers, please use the [public issues section](https://github.com/hjchang/CVPR2015-KinematicStructureLearning/issues) on this github repo. Alternatively, drop us an e-mail at <mailto:hj.chang@imperial.ac.uk>.
