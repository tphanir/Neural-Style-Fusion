# Neural Style Fusion

## Objective
The aim of the project was to implement the **Neural Style Transfer** Algorithm - one of the exciting applications of Convolutional Neural Networks.

## Approach
1. The project started with understanding of Deep Learning and Artificial Neural Networks.
2. With the knowledge of Gradient Descent Algorithm and other primary concepts, we trained a Two Layer Neural Network on MNIST Dataset to classify digits, from scratch using Numpy.
3. Next, we learnt many Optimization Algorithms and tuning of Hyperparameters to refine the Neural Network.Further, we implemented a more efficient Neural Network using the PyTorch Framework to classify the digits.
4. Then, we learnt the working of Convolutional Neural Networks and studied various CNN Architectures.
5. With a good understanding of CNN's, after many trials, we built our own custom architecture on MNIST Dataset that efficiently classify digits with high accuracy.
6. Then we learnt the Neural Style Transfer Algorithm.

## The Algorithm
The technique involves taking two images—a content image(C) and a style reference image(S) (such as an artwork by a famous painter)—and blending them together such that the output image(G) looks like the content image, but “painted” in the style of the style reference image (as shown below).

<img src="https://github.com/tphanir/NeuralStyleFusion/assets/125972587/f66df004-b4a4-4fcd-9809-7f0035691707">

### Procedure
* We first define a Cost Function (J) that measures how good is our generated image (G).
<p align="center">
<img src="https://github.com/tphanir/NeuralStyleFusion/assets/125972587/0d61916c-8038-40e6-9121-792a1c0344e7" >
</p>

* There are two parts to this Cost Function.
    * The first part is called the <i>**Content Loss**</i> function which is a function of the Content Image and the Generated Image.It measures how similar is the contents of Generated image to the content of the Content Image.
    * The second part is the <i>**Style Loss**</i> function which is a function of the Style Reference Image and the Generated Image.It measures how similar is the style of the Generated image to the style of the Style Reference Image
* We have used the pretrained **VGG-19** ConvNet owing to its ability to extract more complex features from both content and style images.
  * The layers marked in red were used to calculate the style of the image S.
  * The layer marked in blue was used to extract the content of the image C.
  
  
  ![NEURAL STYLE FUSION](https://github.com/tphanir/NeuralStyleFusion/assets/125972587/b4177956-cbf7-4ef2-83c7-52aff5b873a5)
   


  


