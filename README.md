# Neural Style Fusion

## Objective
The aim of the project was to implement the **Neural Style Transfer** Algorithm - one of the exciting applications of Convolutional Neural Networks.

## Approach
1. The project started with understanding of Deep Learning and Artificial Neural Networks.
2. With the knowledge of Gradient Descent Algorithm and other primary concepts, we trained a Two Layer Neural Network on MNIST Dataset to classify digits, from scratch using Numpy.
3. Next, we learnt many Optimization Algorithms and tuning of Hyperparameters to refine the Neural Network.Further, we implemented a more efficient Neural Network using the PyTorch Framework to classify the digits.
4. Then, we learnt the working of Convolutional Neural Networks and studied various CNN Architectures.
5. With a good understanding of CNN's, after many trials, we built our own custom architecture on MNIST Dataset that efficiently classifiea the handwritten digits with high accuracy.
6. We then learnt and implemented the Neural Style Transfer Algorithm using PyTorch framework.

## The Algorithm
The technique involves taking two images—a content image(C) and a style reference image(S) (such as an artwork by a famous painter)—and blending them together such that the output image(G) looks like the content image, but “painted” in the style of the style reference image (as shown below).


![New Project (3)](https://github.com/tphanir/NeuralStyleFusion/assets/125972587/9110fc55-247a-4dca-b8c5-960ac96f7fc1)




### Procedure
* A Cost Function (J) is defined that measures how good is our Generated image (G).
<p align="center">
<img src="https://github.com/tphanir/NeuralStyleFusion/assets/125972587/0d61916c-8038-40e6-9121-792a1c0344e7" >
</p>

* There are two parts to this Cost Function.
    * The first part is called the <i>**Content Loss**</i> function which is a function of the Content image and the Generated image.It measures how similar is the contents of Generated image to the content of the Content image.
    * The second part is the <i>**Style Loss**</i> function which is a function of the Style Reference image and the Generated Image.It measures how similar is the style of the Generated image to the style of the Style Reference image
* Pretrained **VGG-19** ConvNet is used to implement the algorithm, owing to its ability to extract more complex features from both content and style images.
  In the network shown below-
  * The feature maps of the Style image extracted from the layers marked in **red** are used to store the style of the Style image.
  * The feature map of the Content image in the layer marked in **blue** is used to extract the content of the Content image.
    
  
<p align="center"><img src="https://github.com/tphanir/NeuralStyleFusion/assets/125972587/0b94c4b7-4559-46f5-bf1b-1eb90567836f"></p>

* A **Gram Matrix** is then calculated which mathematically gives us the correlation between the feature maps of an image, which in simple terms, stores the style of an image.
* Content loss is then found by simply finding the Mean Squared Error between the feature maps of the content and generated images.
* Next, Style loss is calculated as the Mean Squared Error between the gram matrices of the style and generated images.
* The pixels of the Generated image G are then trained to minimize the loss, which implies that the pixels of the Generated Image reach a stage whwere the image looks like the Content image in the style of the Style Reference image.

## Results
* After fine tuning of the parameters, the following results were obtained.

![Results](https://github.com/tphanir/NeuralStyleFusion/assets/125972587/6e29adfa-fba3-4525-a9bd-825082db1375)

* One can infer that if the **Content** and **Style** images are chosen appropriately, the result may turn to be a fanatastic and artistically pleasing image.

## Software Tools used
- Python
- Numpy
- PyTorch
- Torchvision
- PIL
- Matplotlib

  
## How to Run the Project






  


