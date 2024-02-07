# Artistic_Style_transfer_of_images
Style Transfer is a process in which we try to modify the style of an image while preserving its content. Given an input image and a style image, we can compute an output image with the original content but a new style.

More about it on:
https://gsurma.medium.com/style-transfer-styling-images-with-convolutional-neural-networks-7d215b58f461

### How does it work?
1. We take input image and style images and resize them to equal shapes.
2. We load a pre-trained CNN (VGG16).
3. Knowing that we can distinguish layers that are responsible for the style (basic shapes, colors etc.) and the ones responsible for the content (image-specific features), we can separate the layers to independently work on the content and style.
4. Then we set our task as an optimization problem where we are going to minimize:
5. content loss (distance between the input and output images - we strive to preserve the content)
6. style loss (distance between the style and output images - we strive to apply a new style)
7. total variation loss (regularization - spatial smoothness to denoise the output image)
8. Finally, we set our gradients and optimize with the L-BFGS algorithm.

### Content Input:
![image](https://github.com/Sankeerth10/Artistic_Style_transfer_of_images/assets/100099621/5c488e83-345a-4693-ad00-b529863da8bb)

### Style imput:
![image](https://github.com/Sankeerth10/Artistic_Style_transfer_of_images/assets/100099621/2f7a2a07-cf97-4657-83e3-dd0845dfe798)

### Output:
![input1](https://github.com/Sankeerth10/Artistic_Style_transfer_of_images/assets/100099621/b06b6b5b-7e1e-45d2-b6c3-82bdaeebd6f9)
