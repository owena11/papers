
Title:  Self Supervised Video Representation Learning With Odd-One-Out Networks

Authors:  Basura Fernando, Haka Bilen, Efstratios Gavves and Stephen Gould

Publication Status:  Published ICCV 2017

Date of Read:  08 / 04 / 2018

Summary Description: This paper presents a pre-text task base around selecting
the anomalous sample from N presented to the network. Each clip is encoded in
such a way that first layer of the description network is a 2d convolution, with
a Siamese style encoding stack used to deal with the N inputs.  Several simple
forms of motion representation are trailed as input, these include _Sum of
Differences between frames_, _Dymanic Images_, _Stacked Differences of frames_.
Another feature touted of this approach is the lack of needing to carefully
selection of frame from the video. Random sampling of frames is presented, where
the number of frames between selected frames is randomised.  Along with standard
consecutive sampling, and a bunched consecutive sampling strategy.

A similar evaluation process of fine tuning is included in the work to present a
accuracy on UCF-101. The best variant achieve around 60% on split one of UCF,
this is using the _Stack of Differences of frame_ encoding with a random
sampling of training frames from each video. 

Performance on the pre-text task is not incredibly high,`reported at 33.6%
accuracy in the highest case.

Comment: This paper is interesting becasue it uses a motion model as the input
to a task, and build the task at the clip based level. Arguably developing a
better representation that previous pre-text tasks, however it is certainly a
limited motion representation that is being presented to the network.

The throw-away comment that this task would work with other temporal
architectures such as a 3D-CNN is frustrating, as it is a leap to say that this
task provides a strong enough training signal to train the more complex models.
This comment is not supported with any experiments.

Overall it seems to show the promise of temproal models without fully exploiting
the temporal models that exist.

The fine tuning evaluation of the network limits the comparision against other
techniques. Supervised fine tuning of the representation adds in ambiguity to
what gains are learned in the pre-text task vs fine tuning. Makes comparison to
random initialisation the main reference point to compare through.
