# im2txt_demo
im2txt + pretrained models + docker = easy tryout

This repo contains a copy of im2txt (https://github.com/tensorflow/models/tree/master/im2txt), 
a suitable docker image, pretrained models (https://github.com/tensorflow/models/issues/466) and 
some trivial shell scripts for convenience.

### Limitations:
1. The command "git lfs pull" might respond with errors, due to the limited GitHub data quoata. 
  In this case you can 
  - wait until next month and hope you can perform "git lfs pull" before the data limit is reached OR
  - use the above link to the pretrained models and download them manually
2. The tensorflow version is fixed to an old one (0.12). Feel free to update and create a pull request! Thanks in Advance for your help!

### Getting started:

#### Install docker (skip if already installed)
https://docs.docker.com/engine/installation/

#### Clone this repo and pull large files (pretrained models):
```
git clone git@github.com:siavash9000/im2txt_demo.git
cd im2txt_demo
git lfs pull
```

#### build docker image
```
cd im2txt_demo
make build
```

##### start container
```
make run
```

##### build run_inference (must be performed only once)
```
./build_inference.sh
```
##### get caption for image
```
./process_image.sh imgs/bikes.jpg
```
