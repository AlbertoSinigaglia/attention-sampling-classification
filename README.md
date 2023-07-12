# Scaling mega-pixel images classification via attention sampling
In this repository can be found the code to reproduce the code for the case study _Lymphoma subtype classification_ which uses attention sampling to drastically reduce the computational cost of mega pixel image classification

## Highlight
The network is composed by 3 stages:
 - Attention network: sees a downscaled version of the image as says where the information for the classification is likely to be located
 - Patch sampling according to the distribution given by the attention network
 - Classification network: unitary logits vector are extracted by the sampled patches and the final classification is given by a weighted sum of such logits passed though a softmax function

 The attention network is trained using REINFORCE with baseline with and entropy regularizer to overcome the exploration/exploitation dilemma.

## Structure
```
|- presentation.pdf : short presentation of the project
|- report.pdf : the full report of the work done
|- evaluation.ipynb : evaluation of the model
|- project.ipynb : code for the traning
|- model : folder with weights of the model
```

## Dataset
_Lymphoma subtype classification dataset_ downloadable at this [link](https://drive.google.com/file/d/1VRRptGC_1OSRaA_WWl28X0M_Fhtfzjby/view?usp=sharing)

## Credits
[Processing Megapixel Images with Deep Attention-Sampling Models
, arXiv:1905.03711](https://arxiv.org/pdf/1905.03711.pdf)