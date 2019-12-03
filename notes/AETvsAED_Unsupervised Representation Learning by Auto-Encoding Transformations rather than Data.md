# AET vs. AED: Unsupervised Representation Learning by Auto-Encoding Transformations rather than Data

[paper](http://arxiv.org/abs/1901.04596)   [code](https://github.com/maple-research-lab/AET)  

Liheng Zhang(UCF, Phd), Guo-Jun Qi(UCF, Prof.), Liqiang Wang(UCF), Jiebo Luo(UoRochester)

### Main idea:

As long as the unsupervised features successfully encode the essential information about the visual structures of original and transformed images, the transformation can be well predicted.  

### Highlight

The authors present a novel paradigm of unsupervised representation learning by **Auto-Encoding Transformation(AET)** in contract to the conventional **Auto-Encoding Data(AED)**.

This AET paradigm allows us to instantiate a large varity of transformations, from parameterized, to non-parameterized and GAN-induced ones.  

AET sets new SoTA performances being greatly closer to the upper bounds by their fully supervised counterparts on CIFAR-10, ImageNet and Places dataset.  

*AED is based on the idea of reconstrcting input data at the output end. It means a good feature representation should contain sufficient information to reconstruct the input data.*

*AET focuses on exploring dynamics of feature representations under different transformations, thereby revealing not only static visual structures but also how they would change by applying different transformations.*

**AET is kind of summary and sublimation of previous AED methods.**  

### Method

By sampling some operators to transform images, AET seeks to train auto-encoders that can directly reconstruct these operators from the learned feature representations between original and transformed images.

The AET family includes a large variety of transformations. In the paper, the authors discuss three genres:

- **Parametrized Transformations.**  Transformations can be represented by its parameter and the loss between transformations can be captured by the difference in terms of their parameters.
- **GAN-Induced Transformations.** A GAN generator is learned with a sampled random noise z that parameterizes the underlying transformation around a given image x. This effectively defines a GAN-induced transformation with the transformation parameter z. 
  *Compared with the classical transformations that change low-level appearance and geometric structures in images, the GAN-induced transformations can change high-level semantics in image.*
- **Non-Parameterized Transformations.** Even if a transformation is hard to parametrized, they can still define the loss by measuring the average difference between the transformations of randomly sampled images.

While in the paper, the authors focus on the parameterized transformations as they do not involve training extra models like GAN-induced transformations, or require choosing auxiliary transformations to aproximate non-parametric forms.







