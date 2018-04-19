
Title:  PoTion: Pose MoTion Representation for Action Recognition

Authors:  Vasileios Choutas, Philippe Weinzaepfel, Jerome Revaud and Cordelia
Schmid

Publication Status:  Published CVPR 2018

Date of Read: 19 / 04 / 18 

Summary Description: This paper presents the compression of Pose information
into a N channel image, through colourisation and aggregation of pose heatmaps.
Colour is used to encode relative temporal distance, transforming between colour
channels dependent of offset in time. It was unclear on first reading whether
there is a fixed time allocated pre channel or whether each video is split up
into N blocks.

The representation is then passed to a relatively shallow network to classify
the pose representation to a given representation. This is trained independently
of other streams of the networks.

Once combined with I3D the representation produces good numbers on benchmarks
suites. The 2% increase in top-1 precent on charades and 1% on top-5 accuracy
are reported.§ 

Comment: The colourisation technique is an interesting way to include temporal
information in a way that is naturally suited to the standard CNN architecture.
The simplicity of the CNN use introduces questions about how much relevant pose
information is being encodes, why wouldn't a network architecture that is
exceeding in image classification be more suited to this task?

Need to work out whether colourisation is based on fixed windows of a scaled
slice of the whole video. But regardless the use colour as proxy to describe
offset in time, might provide some more interpretable results for the time scale
that network is interested in, what transitions in colour are present in some
sort of activation maximisation visualisation? This might be more interpretable
than the visualisation out of C3D and alike. 

The drop in accuracy for tasks where humans are not fully present in the scene
suggests a limitation in fusion of information from the differing stream of the
network.
