# Fellow_omniglot
One-shot classifier using triplet loss on the omniglot Dataset

# Few-shot learning - Omniglot - Fellowship.ai
This notebook is my personal project to the few-shot learning challenge from [Fellowship.ai](https://fellowship.ai/challenge/) with the following goal:
> Omniglot, the “transpose” of MNIST, with 1623 character classes, each with 20 examples.  Build a few-shot classifier with a target of <35% error.

I managed to reach an error rate of 6.5% on a 20-way classification corresponding to the current state of the art model.

# Abstract


### The Omniglot dataset
*Dataset reference:* [Link](https://github.com/brendenlake/omniglot)
> Lake, B. M., Salakhutdinov, R., and Tenenbaum, J. B. (2015). Human-level concept learning through probabilistic program induction. Science, 350(6266), 1332-1338.

The Omniglot dataset is often considered as the transpose of the MNIST dataset. While the latter contains only 10 classes with a training set of 60000 examples, Omniglot contains an important number of classes (1623 different handwritten characters from 50 different alphabets) with only a low number of examples (20) for each, making it an ideal dataset for few-shot learning problems.

### Few-shot learning
Whereas, lots of deep learning projects are based on a huge number of training examples to be trained, few-shot learning is  based only on a few one. This approach is much closer to the one experienced by humans. We are able to memorize and recognize objects we have never seen before from a few number of examples. Then for each new encounter with these types of object we can classify them in an accurate and easy way.

### Approach
The approach I used for this challenge is essentially based on a triplet-loss model.
For each image one embedding of size 64 was created using a ResNet-like architecture (current state of the art CNN architecture) combined to a triplet-loss  model.