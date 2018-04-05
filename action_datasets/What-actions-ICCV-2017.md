
Title: What Actions are Needed for Understanding Human Actions in Videos?

Authors: Gunnar A. Sigurdsson, Olga Russakovsky and Abhinav Gupta

Publication Status: Published ICCV 2017

Date of Read: 04 / 04 / 18

Summary Description: This paper provides an in detailed analysis of factors that
contribute to the success of an action recognition system. The work is spread
over two distinct section, a human study, assessing the ambiguity in human
interpretation of results and algorithmic evaluations that focuses on how
current algorithms address these properties.

In the human study the following conclusion are drawn:

- Temporal extent is ambiguous to human annotators, with less reliable labelling
  at the end of an action than the beginning.
- Action are less readily confused when considered as a (verb, noun) tuple. The
  example given highlight confusion between (holding, mug) / (drinking mug);
  this is used to justify the importance of a (verb, noun) model of an action
  instead of a purely (verb,) model.

The algorithmic evaluation addresses this model through differences in mAP
over various grouping of videos. Figures 4/5 provide clear examples of this
methodology. The individual insights into algorithms are to numerous to state he
but section 4 of the paper can provide more detail.

They also provide an evaluation of change in mAP with data augmentation,
removing the human figure from the scene using semantic segmentation. Results
shown in figure 8 (b). Similar use of a CNN to group videos based on pose
provides some insight as to how large variations in pose can cause issues for
current networks.

The paper concludes with augmenting two stream with addition "oracle"
information, that is considered as an additional data input to the system
in order to get a baseline for how much information this data contains. The
following information is injected into the system:]

- Object
- Verb
- Intent (High level action context)
- Temporal

Focus on the following datasets:
- Charades
- Multi-THUMOUS

Links:

- [https://arxiv.org/abs/1708.02696](arXiv)
- [github.com/gsig/actions-for-actions](code)


Comment: Overall this feels like a nice explanation of how various factors
affect an action recognition, providing a much broader perspective on this than
the work that we submitted to BMVC (Ice Dancing).

The overall discussion of how to obtain a supervised training signal for your
networks (verb, noun) / (verb,) provides the most question for me, if we need to
define action in this way is it really action recognition? The ability for
objects to be associated with action is an already well studied topic. And I
don't fully understand the confusion metric used to justify the ambiguity in
verbs, it doesn't feel fair to the definition of a verb given how well nouns are
defined.

The human removal can obviously be expanded in the ways that we have discussed
for Ice Dancing work. Although it is clear that we should move this onto the
richer datasets of charades. 
