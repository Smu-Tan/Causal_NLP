## Causal relation detection

In this task, we will explore whether a causal relation can be detected by a NLP model given a sentence. We will use Large Pre-trained Language model as our encoder, then fine-tune it with our data. In addition, after getting the contextualised embedding of the input sentence, it will be pass to a shallow feed-forward neural network. Since huggingface provides a terrific module called BertForClassification, we will adopt it in the experiment.

## Dataset: Semeval-2010-Task 8

### An instance of our data:
#### with entity feature: Most of the <e1> taste <\e1> of strong onions comes from the <e2> smell <\e2>.
#### without entity feature: Most of the taste of strong onions comes from the smell.

[Relation Classification] SemEval-2010 Task 8: Multi-Way Classification of Semantic Relations Between Pairs of Nominals, see: https://arxiv.org/pdf/1911.10422.pdf (#dataset statistics: 10000 totally)

Cause-Effect (CE). An event or object yields an  effect. Example: those cancers were caused  by radiation exposures  (1134 totally)

Instrument-Agency (IA). An agent uses an instrument. Example: phone operator  

Product-Producer (PP). A producer causes a product to exist. Example: a factory manufactures suits  

Content-Container (CC). An object is physically stored in a delineated area of space. Example: a bottle full of honey was weighed 

 Entity-Origin (EO). An entity is coming or is derived from an origin (e.g., position or material). Example: letters from foreign countries  

Entity-Destination (ED). An entity is moving towards a destination. Eg. the boy went to bed 

 Component-Whole (CW). An object is a component of a larger whole. Example: my apartment has a large kitchen 

 Member-Collection (MC). A member forms a  nonfunctional part of a collection. Example:  there are many trees in the forest  

Communication-Topic (CT). An act of communication, written or spoken, is about a topic.  Example: the lecture was about semantics


## experiment planing
![Capture](https://user-images.githubusercontent.com/79228128/144900110-c2605776-6020-4145-bb8f-15969439abb2.PNG)

## Results:
![Capture2](https://user-images.githubusercontent.com/79228128/144900251-33841eb0-60b3-4b2a-926d-835ab09b965b.PNG)
