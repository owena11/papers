
Title:  Learninng  Person Trajectory Representations for Team Activity Analysis

Authors: Nazanin Mehrasa, Yatao Zhong, Fredrick Tung, Luke Bornn, Greg Mori

Publication Status:  MIT SSAC - with expended arXiv Article.

Date of Read: 16 / 08 / 18

Summary Description: This paper presents a technqiue for learning trajectory
representations, based 1D convs over trajectories extracted from optical
tracking. They select a fixed number of people from the frame to describe (5),
and feed these trajectories into the network, pad with 0's where there are not
enough player into it. "Players" are losely defined in this analysis and can
include referees.

The main present novelty presented is forcing comparison to a key player in the
team through concatenation of the intermediate representation for one player
with the other players.

This network is trained through a classication loss, with actions preformed by
the group of players.  In parallel they propose a simplar 1D conv structure to
classify the idendity of the a NBA team given the set of trajectories.

Comment: I really don't understand the intuition between the comparitor
networks, other than pushing it to the forfront of the networks attention, there
is no reason why this can't be encoded with a standard network architecture. And
the choice of a primary actor seems like a massive constraint on the technique.
This leaves alot of space to discuss what can be encoded with the 1D and then
following on, wether a pictoral representation as previously used will a 2D
network more readily encode the information avaliable.
