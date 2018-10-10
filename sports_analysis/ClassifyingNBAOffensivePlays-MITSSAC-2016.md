
Title: Classifying NBA Offensive Plays Using Neural Networks

Authors: Kuan-Chieh Wang, Richard Zemel

Publication Status:  Publised MIT SSAC 2016

Date of Read: 15 / 08 / 18

Summary Description: This paper feeds a 2D pictoral representation into a RNN,
producing a classification result for a certain number of play. The previous
locations of players is included with a decaying trail behind their current
location to provide some additional information at a given time step. Players in
the pictorial representation are labelled with a specific role, based on a
previously learned embedding of their play type.

They demonstrate quick transfer of a model between seasons on play where styles
may have changed. 

Comment: This work is an interesting, the decision to keep a pictorial
representation highlights how important the spatial information is. It's
intriguing that they leave temporal information in the pictoral visualisation,
shouldn't this be captured by the temporal model presented by the RNN.
