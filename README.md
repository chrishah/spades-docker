# spades-docker
Ubuntu 18.04 with SPAdes assembler

The image contains a full install of [SPAdes](http://cab.spbu.ru/software/spades/), including all necessary dependencies. I am not part of the developer team - I just made this image.

In detail, the image is set up with:
 - Ubuntu 18.04
 - SPAdes (v3.14.0)

To run the software you can do the following (this will mount the directory `/in` of the container to the current working directory on your local machine, and allow you to access files in this directory and any sub-directories):
```bash
$ docker run --rm -v $(pwd):/in -w /in chrishah/spades:v3.14.0 spades.py
```

You can also enter the container environment and work within it. All executables should be in the `PATH`.
```bash
$ docker run -it --rm -v $(pwd):/in -w /in chrishah/spades:v3.14.0 /bin/bash
```
