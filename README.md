
Model Architecture

The neural style transfer model leverages the VGG19 convolutional neural network, a widely-used architecture pre-trained on the ImageNet dataset. The VGG19 model is used as a feature extractor, and its intermediate layers are employed to capture both style and content information from input images.

The model architecture is defined using the `get_model` function, which creates a composite model by extracting style and content features from specified layers of the VGG19 model.

Loss Functions

Two key loss functions are utilized to train the neural style transfer model:

1. Content Loss: Measures the difference in content between the generated image and the content image. It is calculated using the mean squared difference between the content features of the two images.

2. Style Loss: Quantifies the difference in artistic style between the generated image and a reference style image. It is computed as a weighted sum of layer-wise style losses, which measure the differences in Gram matrices of style features.

The total loss for training the model is a combination of content and style losses, controlled by weighting factors `alpha` and `beta`:

Adjusting these weighting factors allows fine-tuning of the trade-off between preserving content and adopting style during the optimization process.


