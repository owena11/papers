
Title: Choose Your Neurons: Incorporating Domain Knowledge through Neuron-Importance

Authors: Ramprasaath R. Selvaraju, Preithvijt Chattopadhyay, Mohamed Elhoseiny,
Tilak Sharma,  Dhruv Batra, Devi Parikh and Stefan Lee

Publication Status:  Published ECCV 2018

Date of Read: 24 / Oct / 2018

Summary Description: This paper presents a zero shot learning methodology that
transferred weights developed on a seen dataset to an unseen dataset. This is
done through associating filters with an additional source of knowledge such as
a textual description (converted to a vector through word2vec or attribute
labelling ) at a class level.

Filters are associated attributes of classes through learning of a linear
mapping, that maps some averaged 'importance measure' for that filter on a given
class to the vector of additional knowledge. In this case they use the average
gradient (similar to grad-CAM) with respect to the activation map and
classification scores.

Once this mapping is learned, additional weights can be added to the network to
include classification for the additional classes. These weights are optimised
by ensuring the predicted importance measures for the new class are similar to
those  predicted by previously learned mapping given the knowledge provided on
the unseen class. This is trained on random Imagenet image and the known class
knowledge and expected importance measures.

** This part starts flying over my head conceptually, why should the 'importance
measure' prediction of filters from a random image align with that of a valid
image, as the content is not necessarily there. Is this the cause for the use of
an importance measure, rather than simplify average activations or something
simpler. **



Comment: This seems similar to Tom's pruning work in some respects. The
prediction of later properties is similar in spirit even if it is different in
targeted goal. Need to understand grad-CAM paper to better understand this work
possibly.

Defering to update notes after discussion.
