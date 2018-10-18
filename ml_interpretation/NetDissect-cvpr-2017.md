
Title:  Interpreting Deep Visual Representations via Network Dissection

Authors:  Bolei Zhou, David Bau, Aude Oliva and Antonio Torralba

Publication Status:  CVPR 2017 (Reading extended version of paper presented on
project page)

Date of Read: 17 / 10 / 18

Summary Description: This paper presents a methodology for quantifying the
interpretability of unit (filters) in a CNN. The idea of interpretability is
presented as the count of distinct detectors the methodology is able to
synthesise from the network that align with labels within the 'Broden'
dataset, that is presented alongside the methodology.

The 'Broden' dataset appears to be an amalgamation of datasets that label
various parts of the image over semantic levels. The semantic categories are
as follows, and used as the basis for the future experiments:

 - Scene (468 classes)
 - Object (584 classes)
 - Part (234 classes)
 - material (32 classes)
 - Texture (47 classes)
 - Colour ( 11 classes)

Filters are converted into detectors by observing the their activations over
the entire dataset, and picking a threshold for which that activation is only
fires 0.5% of the time , $T_k$. This threshold is then used to make binary map
of a units activation for a single input. This binary mask is then used to
calculated the Intersection Over Union (IOU) with the labels for every label in
the dataset, if the IOU is over a given threshold (0.04) the unit is considered
a detector for that given category. If a unit is considered a detector for
multiple labels, it is assigned to the label the highest IOU.

Extensive experiments are presented along side this methodology to provide
insight into the behaviour of several choices made within CNN design /
training / usage. Its difficult to summaries all of the experiments due to
their volume, some key notions hinted at are listed below:

 - Interpretability is a normal occurrence within learned weights without
   specialising the network in anyway.
 - Networks generally converge to similar interpretability levels given
   different initialisations.
 - Results match previous results where lower levels represent semantically
   broader labels such as colour.
 - Contrary to other results, high level filters learn semantically distinct
   detectors.
 - Interpretability can be be changed independently from discriminative
   properties of networks.
 - BatchNorm reduces the interpretability of the networks.
 - Self Supervised networks separate less semantic classes than fully supervised
   labels, however components required for the task seems to appear.

~ TBC - sure there is more but difficult to list on first reading, will update
after paper discussion ~

~ Didn't understand the Human experiments, need to re-read ~


Comment: This paper presents an very complete set of experiments, that is
admirable for the breadth of questions they address comprehensively. The
network dissection technique is simple to follow, however appears dependant of
several thresholds, this referenced in the discussion section of the paper.
How does the threshold relate to the distribution of classes across the
datasets? Does it account roughly to the occurrence of the label in the
dataset.

The amalgamation of datasets is an interesting way to gain a more complete
labelling set, although as noted, data is a bottleneck for this interpretation.
It can only exist to detect concepts that exist in datasets, this pushes it
toward finding semantically relevant detectors because its only asked if they
exist or not. This could unfairly penalise networks that have a different
separation of semantic classes or even amalgamations of classes that make sense
for the decisions it is required to make. Such as having a wheel + door
detector as a single unit, would arguably make the network no less
interpretable if the textual description could be given but would be ignored by
this technique.


Bibtext:

``` bibtex
@inproceedings{Zhou2017netdissect,
  title={Network Dissection: Quantifying Interpretability of Deep
         Visual Representations},
  author={Bau, David and Zhou, Bolei and Khosla, Aditya
          and Oliva, Aude and Torralba, Antonio},
  booktitle={Computer Vision and Pattern Recognition},
  year={2017}
}
```
