
Title:  Unsupervised Representation Learning by Sorting Sequences

Authors:  Hsin-Ying Lee, Jia-Bin Huang, Maneesh Singh and Ming-Hsuan Yang

Publication Status:  Published ICCV 2017

Date of Read: 08 / 05 / 2018

Summary Description: This paper presents sorting of frames as a pre-text task
for action recognition, building on the work of Misra et al. The main difference
is in categorical assignment to a tuple of frame ordering rather than binary
decision (N!/2 pairs are considered as they consider actions reversible). They
argue that adding this complexity to the task improves the temporal model
learned by the representation, this is further  expanded by using a pairwise
comparison of frame representations as section of the network. 

They preform the Two-Stream evaluation approach (according to their github
page), however its unclear what representation they actually use for this
evaluation. It is ambiguous which section of the network they use to
form their representation. Whether the representation is sampled prior to the
pairwise comparisons, has an affect on how much of a temporal model is included
in their evaluated work.

_Inspection of their released caffe files or code does not resolve the
ambiguity_

Comment: This paper is interesting for the pretext task that it proposes,
however ambiguity in the evaluation process make it difficult to draw meaningful
discussion from the paper. IF the temporal model (pairwise comparisons) is used,
its interesting to see the inclusion of a temporal model improving results. But
my best guess is that the temporal model is not included based on their
evaluation protocol. This makes the use of the temporal model in learning seem
under exploited; what about the frame representation would be of interest above
the original original order verification task? My hypothesis is that the more
complex task induces better localisation of important objects in the scene for
motion without encoding any motion information itself. 


