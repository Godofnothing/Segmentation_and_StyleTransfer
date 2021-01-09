# Segmentation and StyleTransfer
---

Implementation of localized style transfer from the paper [Localized style transfer](http://cs231n.stanford.edu/reports/2017/pdfs/416.pdf). 

Here the simplified approach is adopted - we do not use the `CRF` (conditional random fields), which are used for smoothing and general improvement of
the segmentation task. 

In order to make a style transfer one needs to pass a content image, obtain a mask on it via evaluation on the pretrained segmentation network, and the style image. 

The current implementation uses `MaskRCNN` with `resnet-50` backbone and `vgg19` backbone for the style transfer. 

Function from `detection` directory are copied from [PyTorch vision] https://github.com/pytorch/vision
