
Title:  Chanined Multi-stream Networks Exploiting Pose, Motion and Appearance
for Action Classification and Detection

Authors:  Mohammaderza Zolfaghari, Gabriel L. Oliveira, Nima Sedaghat and
Thomas Brox

Publication Status: Published ICCV 2017

Date of Read: 05 / 04 / 2018

Summary Description: This work proposes the use of a three stream 3D CNN in
order to capture the relevant spatial-temporal characteristics of an action. The
focus on using Pose / Optical Flow and RGB.

Videos are fed to the network sequentially as 16 frame blocks, with a time step
of 8. Random cropping is used in the test stage of the paper, averaging the
softmax scores of 10 crops + n time steps. Pose for each video is calculated
using fastnet` a independently train pose detection network.

Fusion of features is where the main novelty in the paper is reported,
sequentially combining time steps and streams of the network to provide a better
fusion of information. This is compared against the baseline of concatenation.

The paper reports improvments on HMDB51 compared with contempary works (TSN),
however does not provide advances on UCF101. These are the primary comparative
datasets used within the work.

Comment: I don't fully understand the motivations of including specific pose
stream seperate from RGB+Flow. If the conceptual model of the 3D CNN generating
a hierachy of spatial-temporal features what is the advantage of the pose
networks? although it does result in higher benchamark scores in certain
scenarios.  It seems as the lack of improvement over LTC on UCF 101 supports
this suspicion.

The differences between the more complex feature agregation method appear to
have marginal benifits over benchmarks.
