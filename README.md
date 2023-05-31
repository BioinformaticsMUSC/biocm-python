# biocm-python docker image

This is a Dockerfile for a python-based image for bioinformatics analysis, with tools based around the Scanpy framework. 

## For local use

You can use Docker to pull the image and create a container (make sure you have Docker installed and running):

```
docker run -it bioinformaticsmusc/biocm-python:latest /bin/bash
```

Make sure you are on a compute node in the palmetto cluster.

Navigate to the `singularity_images` folder:
```
cd /zfs/musc3/singularity_images
```

Use the following command to open an R command prompt:

```
singularity shell -B /zfs/musc3:/mnt --pwd /mnt biocm-python_latest.sif
```
Note the options used here:
- `-B /zfs/musc3:/mnt`: this command creates a link between the source directory (here, `/zfs/musc3`) and the destination directory inside the 
container `/mnt`. You may link any 
source directory--those directories and files will then be accessible inside the container. If you save anything within those directories inside the 
container, it will exist when 
the container is done. 
- `--pwd /mnt`: this sets the working directory inside the container to `/mnt`, which is the mounted volume linked to the source directory.


### What's new

05/31/23
Version 1.1.0
- Installed cnmf for Consensus Non-negative Matrix Factorization and squidpy for spatial transcriptomics analysis


