# Using Self-Supervised Learning Can Improve Model Robustness and Uncertainty

[link](http://arxiv.org/abs/1906.12340)

Dan Hendrycks(UCB), Saurav Kadavath(UCB), Mantas Mazeika(UIUC), Dawn Song(UCB) 

### Highlight

This paper shows findings about combine self-supervised learning with supervised learning can improve model's performance on robustness and uncertainty. It serves like a summary with experiments.

In this paper, they found self-spervision can:

-  improve model's **robustness** to **adversarial examples, label corruption and common input corruptions**. 
- benefits **out-of-distribution** (OOD) detection on difficult, near-distribution outliers

This paper has essentially no theory, but proposes lots of interesting directions for future work. 

### Method

The self-supervised method used in all the experiments is an auxiliary rotation-based self-supervision which predict image rotations. (This method comes from Gidaris et al. 2018).

For different tasks, their methods setting are varied. But in terms of core technology, they train a classification network along with a separate auxiliary head, which takes the penulimate vector from the network as inout and outputs a 4-way softmax distribution. This head is trained along with the rest of the network to predict the amount of rotation applied to a given input image (from 0 degree, 90 degree, 180 degree and 270 degree). As a result, they modifed the overall loss.

### 



