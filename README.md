# w251-hw5: Deep Learning Frameworks - Training an image classifier on the ImageNet 2012 dataset from random weights.

### The goal
The goal of the homework is to train an image classification network on the ImageNet dataset with PyTorch.

### The steps
The steps are roughly as follows:

1. Procure a virtual machine in AWS - we recommend a T4 GPU and 1 TB of space (e.g. g4dn.2xlarge). Use the Nvidia Deep Learning AMI so that the pre-requisites are pre-installed for you. We recommend using the latest [nvidia pytorch container](https://ngc.nvidia.com/catalog/containers/nvidia:pytorch)
2. Download the ImageNet dataset to your VM. Please do register at [image-net.org](https://image-net.org/challenges/LSVRC/2012/index.php) for all of your future needs. Given the slowness of download via this web site, however, we have downloaded a copy of ImageNet for you and will distribute it in class. (FYI - some students found [this link](https://github.com/facebookarchive/fb.resnet.torch/blob/master/INSTALL.md#download-the-imagenet-dataset) helpful for downloading)
3. Prepare the dataset:
  * create train and val subdirectories and move the train and val tar files to their respective locations
  * untar both files and remove them as you no longer neeed them
  * Use the following [shell script](https://raw.githubusercontent.com/soumith/imagenetloader.torch/master/valprep.sh) to process your val directory. It simply moves your validation set into proper subfolders
  * When you untarred the train file, it created a large number (1000) of tar files, one for each class.  You will need to create a separate directory for each of class , move the tar file there, untar the file and remove it. This should be a one liner shell script but we'll let you have fun with it!
  * Make sure that under the train and val folders, there is one directory for class and that the samples for that class are under that directory
5. Adapt the code we discuss in the labs to the training of imagenet. Make sure the number of classes and image sizes are correct. Make sure the transforms are correct.
6. Start training && observe progress !
