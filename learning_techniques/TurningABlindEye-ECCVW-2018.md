
Title:  Turning a Blind Eye: Explicit Removal of Biases and Variation from Deep
Neural Network Embeddings

Authors: Mohsan Alvi, Andrew Zisserman and Christoffer Nellåker

Publication Status: Workshop Workshop on Bias Estimation in Face
Analytics, ECCV, 2018

Date of Read:  10 / 10 / 2018

Summary Description: This paper presents an augmented learning technique to
remove biases explicitly from a dataset where suplemental labels exist. A two
step learning process is proposed:

 - Firstly the bias of the feature reprsentation is estimated by training a
   classifier for the bias porperty.
 - Secondly the main loss which is a sum of its ability to preform the main
   task and confuse the previously trained bias classifier.

This two step is repeated until convergance. This method is demonstrated to
work within the context of fine tuning weights on different datasets, in this
case taking VGG-M architecture pretained with VGG-Face weights. This is then
specialised for thier other tasks that are trained several other face datasets.

The networks parameters are subdivited into severeal frozen and unfrozen
section in order to speed up training, and anacdotally reported to have
minimunm affect on training.

 - Convs 1 - 5 frozen
 - Fc6 - fc7  θ\_feature
-  Fc 8 levels duplicated to make  θ\_main and θ\_bias

Implemented in matconvnet

Comment:  This paper is provides an interesting explicit bias removal technique
, however the way it references other highlights my lack of knowledge in the
area.

The data cleaning methodology gives me cause for concern, the use of black box
API to give concensus makes me question what datasets that API was trained on.
How can we validate that this is a reasonable methodology for cleaning the
dataset, and doesn't leverage the biases that are already exist within the
dataset.

The experiments preformed do not convince me that this could be inmplemented
from scratch training of a network. Complemented by the relatively restricted
part of the networks being used to preform the experiment - Is the claim they
are modifiying the feature representation or the classifier? If they claim is
they are modifiying the features a scratch trained classfier on extracted
feature reps would be a more convincing arguement. This addressed by the T-SNE
presented within the paper, but I'm hesitant as to how much it safe to read
into as T-SNE diagram.

I struggled to understand the key takeaways on initial reading of the paper.
