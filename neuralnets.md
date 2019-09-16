# Neural Networks (NNs)
As long as you don't live under a rock in a remote island on a planet other than Earth, you're bound to have heard of the *Neural Network*. Ask any self-proclaimed expert ELI5 explanation of NNs & they'll tell you that it is an insanely simplified emulator of a human brain- a network of nodes that pass information through from an arbitrary beginning to an end, each one applying a simple mathematical function to the information. So you think the concept of NNs is pretty interesting- a model that can approximate nearly any function? Who wouldn't be interested?!

So, you decide to explore it a bit more. Maybe you take a course or two on it, watch several YouTube videos on it, follow along through a couple of articles. By this point, you feel sufficiently confident with your skills, thinking that you're about ready to build something revolutionary, solve a pressing problem. As you delve into this, you quickly realise- there is _so much more_ to NNs. You learn that NNs, much like our brains, are incredibly complex structures with hyperparameters upon hyperparameters to consider. Past a certain point, you come to terms with the fact that you aren't, in fact, anywhere close to being an expert. & so you sit yourself down & prepare yourself for a deep dive into NNs unparalleled to anything you've done before. You open up a fresh document, ready to absorb everything the wide web has to offer.

This is that document.



## Hyperparameter Optimization
As illustrated at length above, the architecture & subsequently performance of a NN is, in essence, derived from the set of its hyperparameters. This creates an importance for us to define the optimal set of hyperparameters. However, the problems we often aim to solve with NNs are not only highly complex, but also differ greatly. This means that it is challenging to outline a blueprint or set of rules to abide by when choosing these hyperparameters. Thus, we find ourselves in a bind. We have a problem that we know can be solved with a carefully designed NN. However, we don't know how to design the NN.

This is exactly where the task of **Hyperparameter Optimization** comes in. We can't tell you which hyperparameters to use from the get-go, but we can tell you how to find them.

### Hyperparameter Selection Methods
There are several methods you could choose from, each with their set of merits & faults. 

#### Grid Search
This is the naive, simplistic method of optimizing your model's hyperparameters. Simply define the range of values for all the hyperparameters you'd like to search over & then train the model for all combinations of these parameter values. You can then select the best model that results from this process.

As you'd expect, however, this method is really only feasible if (a) the model trains quickly & (b) there is a relatively small set of parameters to train. For a quick example to illustrate the infeasibility of grid search- assuming a NN with 5 parameters to optimise, each one from a set of 10 values. For a model that trains, on average, in 10 minutes, grid search would take **nearly 2 years**. The main contributing factor to this is perhaps the fact that a whopping 100,000 evaluations have to completed.

#### Random Search
Given what we know about grid search, perhaps we decide to not evaluate every possible combination of hyperparameter values. Instead, we use a randomly selected subset of the parameter values. However, it could easily be seem how random sampling may not be fully representative of the parameter space. To solve this, we can make use of quasi-random sequences, that fill n-space more uniformly than uncorrelated random points. Do note, however, that certain quasi-random sequences don't work well for parameter spaces beyond 10 dimensions.

Employing this method could prune the search space down from 100,000 permutations to a much more modest 1,000 permutations. The previous ETA of nearly 2 years is therefore cut down to about a week.

Still, though, we cannot help but ask ourselves- *is random search really the best method to tackle hyperparameter optimization?* As AI researchers & experts around the world have found, random search can, indeed, be bested. The following points illustrate this.

#### Hand-tuning
This next method is suited to actual ML experts with troves of experience working with NNs. At their level, they have an intuition for what is needed of their model, & are able to quickly land upon the optimal set of hyperparameters for their model.

Howbeit, I'm going to presume that you're reading this at all precisely because you aren't yet an **ML Expert** & do not yet have this intuition. In that case, perhaps the following methods can prove to alleviate the headache that comes with thinking about hyperparameter optimization.

#### Bayesian Optmization
There are a number of algorithms that apply this same idea. Here, I'll focus specifically on the **Gaussian Process with Acquisition Function**. The overarching principle driving this algorithm closely resembles that of the above hand-tuning method- the algorithm is given a set of previously evaluated parameters & resulting accuracy & attempts to predict the next set of parameters that should results in an increase in accuracy. 

##### Gaussian Process


##### Acquisition Function


#### Tree-structured Parzen Estimators (TPE)


# Resources used
NeuPy. Hyperparameter optimization for Neural Networks. 2016-12-17. http://neupy.com/2016/12/17/hyperparameter_optimization_for_neural_networks.html

Oscar Knagg. An intuitive guide to Gaussian processes. https://towardsdatascience.com/an-intuitive-guide-to-gaussian-processes-ec2f0b45c71d