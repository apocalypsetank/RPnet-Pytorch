# PyTorch-RPNet

PyTorch implementation of [* Residual Pyramid Learning for Single-Shot Semantic Segmentation *](https://arxiv.org/abs/1903.09746)

This implementation has been tested on the Cityscapes and CamVid (TBD) datasets. Currently, a pre-trained version of the model trained in CamVid and Cityscapes is available [here](https://github.com/superlxt/RPnet-Pytorch/tree/master/save).


|                                Dataset                               | Classes <sup>1</sup> | Input resolution | Batch size |    Epochs  |    Mean IoU (%)   |
|:--------------------------------------------------------------------:|:--------------------:|:----------------:|:----------:|:----------:|:-----------------:|
| [CamVid](http://mi.eng.cam.ac.uk/research/projects/VideoRec/CamVid/) |          11          |      480x360     |      3     |   300 x 4  |       64.82       |
|           [Cityscapes](https://www.cityscapes-dataset.com/)          |          19          |     1024x512     |      3     |   300 x 4  |     70.4 (val)    |

* When referring to the number of classes, the void/unlabeled class is always excluded.<br/>
* Just for reference since changes in implementation, datasets, and hardware can lead to very different results. Reference hardware: Nvidia GTX 1080ti and an Intel Core i7-7920x 2.9GHz. 


## Installation

1. Python 3 and pip.
2. Set up a virtual environment (optional, but recommended).
3. Install dependencies using pip: ``pip install -r requirements.txt``.



### Examples: Training

```
sh train.sh
```

### Examples: Testing

```
python main.py -m test --step 1
```

