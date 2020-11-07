# Model-Agnostic Boundary-Adversarial Sampling for Test-Time Generalization in Few-Shot learning

> Link: [ECCV 2020](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123460579.pdf)

## 1. Background
### 1.1 Few-shot problem
Few-shot learning is a general name for tasks in which people hope to train a machine learning model with just very small amount of data.

### 1.2 Previous Research
1. ***Data augmentation***. Generating fake labaled data.
2. Distance metric methods 
3. Meta-learning methods 

### 1.3 Limitations of data augmentation few-shot
1. Such methods learn to generate additional examples with the meta-training set, and thus may not be effective if meta-test domains are far from the meta-training domain.
2. Since they do not update the trained parameters of the base classifier models at test time, they have no chance to correct the errors that exist in the base classifiers (e.g. overfitting of the embedding functions to the meta-training set).
3. These methods need to be re-trained for each base classifier to generate fake labeled data optimal for the base model.

## 2. Innovative Designs
A novel model-agnostic sample generation approach named **MABAS** (Model-Agnostic Boundary-Adversarial Sampling). 
### 2.1 Test-time Fine-tuning of Embedding Functions
Since each meta-test task consists of the classes that are never seen during metatraining, it is a common approach in few-shot learning to fine-tuning the learned parameters using the support samples of the novel task. This work 
