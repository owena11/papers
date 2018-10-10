
Title: Moments in Time Dataset: One Million videos for event understanding

Authors:  Mathew Monfort, Bolei Zhou, Sarah Adel Bargal, Alex Andonian, Tom Yan, Kandan Ramakrishnan, Lisa Brown, Quanfu Fan, Dan Gutfruend, Carl Vondrick and Aude Oliva

Publication Status:  Unpublished, competition inline with CVPR 2018 ActivityNet workshop.

Date of Read:  18 / 04 / 2018

Summary Description: This paper presents a dataset of 1 Million 3 second clips
of video, each associated with a single verb. Verbs we selected based on
popularity within language, clustered into subcategories; example verbs include
'Dancing', 'Crashing', 'sniffing' and 'injecting'.

Videos were retrieved from online services (Youtube, FLickr, Vine, Metacafe,
VideoBlocks, Bing and Giphy). Videos we selected by crawling search engines and
associated metadata. After initial selection a 3 second clip is randomly
selected and passed to human annotators for binary labelling of whether that
_verb_ is occurring in the presented 3 second clip.

Baseline algorithms are presented and compared against a top-5 accuracy. Several
popular network architectures are addressed, including some fine tuned on static
representation (places / objects).  Characterisation of diversity within the
dataset is provided through detection of locations/objects using places365 and
imagenet trained networks respectively.

Comment: The source of labelling coming from verbs is an interesting tact, it
allows nice descriptive labels that nicely fit within the binary classification
system presented to human annotators. The charaterisation of the dataset
provides a good idication that there is a diverse range of videos within the
dataset. Strange that the baseline methods are computed on different sized
videos to the precompressed videos avaliable.

Links: [Dataset website](http://moments.csail.mit.edu/)

