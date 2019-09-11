# Neural Networks (NNs)
As long as you don't live under a rock in a remote island on a planet other than Earth, you're bound to have heard of the *Neural Network*. Ask any self-proclaimed expert ELI5 explanation of NNs & they'll tell you that it is an insanely simplified emulator of a human brain- a network of nodes that pass information through from an arbitrary beginning to an end, each one applying a simple mathematical function to the information. So you think the concept of NNs is pretty interesting- a model that can approximate nearly any function? Who wouldn't be interested?!

So, you decide to explore it a bit more. Maybe you take a course or two on it, watch several YouTube videos on it, follow along through a couple of articles. By this point, you feel sufficiently confident with your skills, thinking that you're about ready to build something revolutionary, solve a pressing problem. As you delve into this, you quickly realise- there is _so much more_ to NNs. You learn that NNs, much like our brains, are incredibly complex structures with hyperparameters upon hyperparameters to consider. Past a certain point, you come to terms with the fact that you aren't, in fact, anywhere close to being an expert. & so you sit yourself down & prepare yourself for a deep dive into NNs unparalleled to anything you've done before. You open up a fresh document, ready to absorb everything the wide web has to offer.

This is that document.



## Hyperparameter Optimization
As illustrated at length above, the architecture & subsequently performance of a NN is, in essence, derived from the set of its hyperparameters. This creates an importance for us to define the optimal set of hyperparameters. However, the problems we often aim to solve with NNs are not only highly complex, but also differ greatly. This means that it is challenging to outline a blueprint or set of rules to abide by when choosing these hyperparameters. Thus, we find ourselves in a bind. We have a problem that we know can be solved with a carefully designed NN. However, we don't know how to design the NN.

This is exactly where the task of *Hyperparameter Optimization* comes in. We can't tell you which hyperparameters to use from the get-go, but we can tell you how to find them.

### Hyperparameter Selection Methods
There are several methods you could choose from, each with their set of merits & faults. 

#### Grid Search
This is the naive, simplistic method of optimizing your model's hyperparameters. Simply define the range of values for all the hyperparameters you'd like to search over

#### Random Search


#### Hand-tuning


#### Gaussian Process with Expected Improvement


#### Tree-structured Parzen Estimators (TPE)


