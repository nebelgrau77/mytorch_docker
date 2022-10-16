## PyTorch & Jupyter Lab container

Simple docker container for experimenting with PyTorch. 

### Features: 

- built on top of the official `pytorch/pytorch` image. 
- launches a Jupyter Lab session. 
- CUDA support is available, i.e. GPU visible from the container (`nvidia-docker2` should be installed on the host).
- mounts a `notebooks` volume for storage on the host

### To do: 
- add a custom start URL
- add a simple website as interface for when accessed from another machine (e.g. links to "Lab" and "Notebook")

