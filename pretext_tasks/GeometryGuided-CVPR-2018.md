
Title:  Geometry Guided Convolutional Neural Networks for Self-Supervised Video
Representation Learning

Authors:  Chuang Gan, Boqing Gong, Kun Liu, Hao Su and Leonidas J. Guibas

Publication Status:  Published CVPR 2018

Date of Read: 03 / 05 / 18

Summary Description: This paper proposed use of optical flow and image
displacement (flow only in the X plane) as an initialisation. They argue that
the use of synthetic data from 3D scenes and 3D movies allows this to function
as a pre-text task.

This networks is then fine-tuned for the action recognition through a multi-stage
learning procedure.

Comment: This approach doesn't convince me that this is a good pre-text task, it
seems closer in spirit to an initialisation technique, in which ActionFlowNet
makes a more compelling argument for use of flow.

It would have been more convincing to see a fine tuning from a FlowNet style
network trained on a more complete flow task. The simplicity of flow task is
justified through the generation of ground truth; with the 3D offset task trying
to push the data as closer to natural input, however this only further
highlights the problems associate with synthetic data that hampers its use as a
pre-text task. The data is no where near as readily present as other
pre-text tasks present in the literature.

Transfer of flow information from an external algorithms is show to be more
effective (see ActionFlowNet).

