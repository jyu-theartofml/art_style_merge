#### Background Info

The purpose of this post is to test the code presented in Siraj Raval's youtube video on artistic style transfer onto photos.
https://www.youtube.com/watch?v=Oex0eWoU7AQ\

Raval's code can be found at his github --> https://github.com/llSourcell

#### Setup of AWS EC2 instance

The jupyter notebook was ran via EC2 instance g2.2xlarge with Udacity Tensorflow AMI (ami-e6ade686). This AMI is equipped with CUDA, GPU support, Keras, Tensor Flow, Python 2.7 and jupyter notebook. However, the jupyter notebook config file needs to be edited to allow browswer access at the ip address via port 8888. Furthermore, Keras doesn't automatically recognize Tensorflow as default backend. In launching the notebook, use the following command flag to dynamically switch the backend:

KERAS_BACKEND=tensorflow jupyter notebook

Looking at the content image (flatiron2) and style image (ezanne.gardanne), it appears that the content image did not have a wide enough range of pixel values/color contrast to result in a good mapping of the style image. It's easy to tell the darkest hue from the style image was mapped to the darkest hue of the content image, but the final merged image lacked the range of the original image. Also, performing this kind of optimization using the VGG16 architecture took a long time on the CPU, GPU integration is highly recommended. 

#### Platforms of artistic style transfer

There's a few companies out there that built a business model around artistic style transfer using more sophisticated algorithms, and pretrained network on tons of images. The most popular one is the Prisma app (https://prisma-ai.com/) and Deepart (https://deepart.io/)
