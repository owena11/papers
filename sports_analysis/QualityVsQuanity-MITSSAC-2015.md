
Title: "Quality vs Quantity": Improved Shot Prediction in Soccer using Strategic
Features from Spatiotemporal Data

Authors: Patrick Lucey, Alina Bialkowski, Mathew Monfort, Peter Carr and Iain
Matthews 

Publication Status: Published MIT SSAC

Date of Read:  15 / 08 / 18

Summary Description: This paper proposes several hard crafted features to be
fed into a  conditional random field (CRF) in order to predict the likelihood of
a goal being scored given a play. This technique is evaluated with an 'error'
when compared to observed events, however I am not entirely sure how this error
is defined.

 The had crafted features encode several features that the authors believe to be
to be important to the chance of a goal happens. This includes role assignments
of players using their previously work, and relative positions to defending
players. 10s of spatio temporal tracks are also used to obtain the final play
evaluation.  The value calculated is some approximation of expected goal value
(xG). 

Comment: No real comment on this paper, it interesting within the context of the
work current work. Presenting the idea that there is some expectation of an
event happening given the current circumstances nicely quantifies some aspects
of the game that are harder to encode. 
