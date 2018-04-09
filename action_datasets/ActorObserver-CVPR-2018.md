
Title: Actor and Observer: Joint Modeling of First and Third-Person Videos

Authors: Gunnar A Sigurdsson, Abhinav Gupta, Cordelia Schmid, Ali Farhadi and
Karteek Alahari.

Publication Status: Published ICCV 2017

Date of Read:  This paper introduces the Charades-Ego dataset, that provides
paired recording of actors preforming a script from first and third person
perspectives.  It uses a triplet loss to learn a unified representation of the
two sources, ranked by a so called selector function that encodes relative
importance of two frames within a video.

The anchor point is always chosen to be a 3rd person video, with positive and
negative examples coming from first person examples. ResNet 152 pre-trained on
he original charades dataset is used at the initialisation for this network.

*Need to read more about the evaluative section on this paper*

Summary Description:

Comment: The selection of the anchor from a certain subset must limit the space
that the network learned, almost aligning the two spaces assuming a sutible
structure is learned form the initialisation.
