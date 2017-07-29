#### The purpose of this post is to test the code presented in Siraj Raval's youtube video on artistic style transfer onto photos.
https://www.youtube.com/watch?v=Oex0eWoU7AQ\

Raval's code can be found at his github --> https://github.com/llSourcell

#### Setup of AWS EC2 instance

The jupyter notebook was ran via EC2 instance g2.2xlarge with Udacity Tensorflow AMI (ami-e6ade686). This AMI is equipped with CUDA, GPU support, Keras, Tensor Flow, Python 2.7 and jupyter notebook. However, the jupyter notebook config file needs to be edited to allow browswer access at the ip address via port 8888. Furthermore, Keras doesn't automatically recognize Tensorflow as default backend. In launching the notebook, use the following command flag to dynamically switch the backend:

KERAS_BACKEND=tensorflow jupyter notebook
