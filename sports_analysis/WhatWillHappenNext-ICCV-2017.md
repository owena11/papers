
Title: What will Happen Next? Forecasting Player Moves in Sports Videos

Authors:  Panna Felsen, Pulkit Agrawal, Jitendra Malik

Publication Status: Published ICCV 2017

Date of Read:  15 / 08 / 18

Summary Description: This paper describes a dataset (not easily obtainable at
time of writing), along with several baseline techniques for recognising actions
within the videos. The concept of using future frame prediction for additional
training with classification.  The dataset consists of 5 games of water polo, as
well as  82 basketball matches with associated SportsVU data. Each game is
annotated with relevant events for the specific sport.

A baseline of human prediction of events is presented for the water polo games,
generate by 9 lay / 4 expert observers of clipped videos.

The paper also explores the forecasting of events within the dataset, through
the use of hand crafted feature set w/ random forest and end to end through some
network architecture. Hand crafted features are based of a automatically
generated 'whiteboard' view of the game, generated through tracking (by
detection) player in the game and projecting their location into a synthesised
image.

An end to end system is also proposed, where some network architecture is train
to forecast the future events. They ultimately find this model under preformed
when compared to the hand crafted approach. Forecasting in this scenario is
presented as a classification of which one of the labelled events happens
$T$ seconds after the clip encoded.

Some generality of the random forest is shown between basketball and water polo,
with selection of the pass receiver producing an accuracy on par with the baseline
of most 'open' teammate.

Ball location is also proposed as a task for the CNN to preform.

Comment: The dataset proposed in this paper seems of interest. However I'm not
fully convinced by the conclusions drawn by the paper, it would have been
interesting to see the result of passing the hand engineered features to a NN to
have a greater understanding of where the end to end system was failing. Was it
unable to learn a meaningful intermediate representation? Or was it just ill
suited to the classification problem at hand for some reason?

The use of temporal  ball location prediction is interesting, and feeds into
pre-text tasks that might be of use within a game prediction scenario, although
this task is dependent on the SportsVU people.
