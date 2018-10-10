
Title:  Tracking Emerges by Colorizing Videos

Authors: Carl Vondric , Abhinav Shirastava, Alireza Fathi, Sergio Guadarrama,
Kevin Murphy

Publication Status:  Published  ECCV 2018

Date of Read:  14 / 08 / 18

Summary Description: This paper uses colourisation of an image from a reference
frame as a pre-text / self-supervised task for various formulations of a tracking
task. An attention mechanism is used to to form a pointing mechanism between the
reference frame and the target frame, it is the repurposing of this attention
mechanism that forms the basis of the tracking mechanism.

Each frame is embedded using Res-Net 18, and then passed on to a further
temporal embedding network. This temporal embedding constitutes the similarity
that the attention mechanism is built on, the temporal embedding is passed to
the attention mechanism to find the contribution of each pixel to it's
colourisation. 

Colour is heavily discretized into categorical values, the weighted combination
of the pixels pointed to by the attention mechanism in the colour space is used
to form the predicted label for colourization. This is then compared to the
ground truth pixel value using categorical cross entropy to from a loss that is
back propagated through the network. 


Implementation details:
 -  Adam is used as the optimiser.
 - lr 0.001 for the first 60,0000 iterations, then dropped to 0.0001 for the
   remaining 340,000 iterations. Batchsize of 32.
 - The train set of the kinetics dataset is used to for training the colourisation
   model. With videos sampled a 6fps.
 - Lab colour space used for quantisation.
 - No pooling, video are reduced in dimension by stride in the convs instead.
 - Input to the network is all grey scale, however the loss is calculated based
   on the colourised labels available after the attention mechanism.
 - Temporal model is based on 4 frames. Loss is calculated for 3 references
   frames with 1 target at each stage in the model. 

Comment: This paper provides a very interesting task for pre-text, and differs
from most other pre-text tasks in the way it reuses part of the network
structure instead of purely the representation, the representation is instead
forced to be useful in the network mechanism. This level of indirection sets it
apart from other pre-text tasks.

Its interesting that no spatial constraint is needed in order to focus local
pointing to occur, it just emerges naturally.

The use of the temporal model, allows the representation to be built of a
combination of multiple target and reference frames. Initially this seems
concerning that some in information might leak betweek the two sets, however 
with the indirection though the attention mechanism reduces this concern.
The small (4) temporal window makes me question whether this is adding
much, and that access to both reference frame and target frame provides the
majority of the benefit.
