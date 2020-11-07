# Generalizing from a Few Examples: A Survey on Few-shot Learning

## 1. General Discription of Few-shot
### 1.1 Definition of Few-shot 
> **Few-shot Learning** (FSL) is a type of machine learning problems (specified by E,T, and P), where E contains only a limited number of examples with supervised information for the target T.

## 2 FSL Taxonomy 
FSL could be divided into three areas: data, model, and algorithm.

### 2.1 Data FSL
FSL uses prior knowledge to augment data D<sub>train</sub>, which can enrich the supervised information. 

#### 3.1 Transforming Samples from a Weakly Labeled or Unlabeled Data Set
This strategy augments D<sub>train</sub> by selecting samples with the target label from a large data set, which is weakly labeled or unlabeled.

*For example, in photos taken by a surveillance camera, there are people, cars and roads but none of them are labeled. It would also happen if there's a video for long presentation, which contains a series of gestures of the speakers, whereas none of those speakers.*

1. An exemplar SVM is learned for each target label in D<sub>train</sub>, which is then used to predict labels for samples from a weakly labeled data set. Samples having the target labels are then added to D<sub>train</sub>. <br>[T. Pfister, J. Charles, and A. Zisserman. 2014. Domain-adaptive discriminative one-shot learning of gestures. In Proceedings of the European Conference on Computer Vision. 814–829.](https://www.researchgate.net/publication/273316702_Domain-Adaptive_Discriminative_One-Shot_Learning_of_Gestures) 
2. Instead of learning a classifier, label propagation is directly used to label an unlabeled data set. <br>[M. Douze, A. Szlam, B. Hariharan, and H. Jégou. 2018. Low-shot learning with large-scale diffusion. In Proceedings of the Conference on Computer Vision and Pattern Recognition. 3349–3358.](https://arxiv.org/abs/1706.02332)
3. A progressive strategy is used to select informative unlabeled samples. The selected samples are then assigned pseudo-labels and used to update the CNN. <br>[Y. Wu, Y. Lin, X. Dong, Y. Yan, W. Ouyang, and Y. Yang. 2018. Exploit the unknown gradually: One-shot video-based person re-identification by stepwise learning. In Proceedings of the Conference on Computer Vision and Pattern Recognition. 5177–5186.](https://openaccess.thecvf.com/content_cvpr_2018/html/Wu_Exploit_the_Unknown_CVPR_2018_paper.html)