This blog post assumes a basic understanding of convolutional neural networks and deep learning concepts, as well as a general understanding of reinforcement learning. For an introduction, I recommend _________ and _______.
Generative models and reinforcement learning techniques both address very common, very compelling problems in machine learning. Generative models address problems like data sparsity (an insufficient number of samples with which to train a model) and more generally, the problem of generating samples from an extremely high-dimensional or otherwise multimodal probability distribution, without having a good idea of a loss function with which to judge those samples.
    Reinforcement learning generally addresses the problem of optimizing policies (in a given state of an environment, what is the optimal action to optimize some reward function); however, due to the complexity of the state and action space (and consequently, the number of possible state-action pairs which the learner would have to keep track of), as well as the complexity of the relationship between a series of state-action pairs and the overall effect on the reward signal, reinforcement learning also suffers from the problem of capturing an incredibly high dimensional signal-over-time (the reward signal), without having any immediately available information on the underlying interactions affecting the value signal. In some of the reinforcement learning methods this series will cover, the value signal is not even given! Expert state-action pairs, or sequences of state-action pairs, are given in its stead, and a naive solution to the lack of a value function is inverse-reinforcement learning, in which a value function is learned from these state-action pairs. Wouldn’t it be nice to learn directly from expert data, if it’s available, though?
    There appears to be some overlap in the problems addressed by generative models and reinforcement learning models - they both seek to either model or interact with a distribution which would require a tremendous amount of information (or samples) to fully capture! The best either model can do is approximate the distribution, typically with a neural network - and the methods which achieve this for each task appear to be quite similar, or at least quite related. 
    This series will be focusing on generative neural network models in which the loss function the generator is attempting to minimize is an adversarial network - that is, a network which is in direct competition with the generator network. The baseline model for this approach to generative models is referred to as a Generative Adversarial Network (GAN) - a good introduction to GANs can be found __________ (the paper introducing GANs is quite accessible as well). 
