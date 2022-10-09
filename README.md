## PyTorch & Jupyter Lab container

Simple docker container for experimenting with PyTorch. 

### Features: 

- Built on top of the official `pytorch/pytorch` image. 
- Launches a Jupyter Lab session. 
- CUDA support is available, i.e. GPU visible from the container (`nvidia-docker2` should be installed on the host).
- mounts a `notebooks` volume for storage on the host

### To do: 
- have a single point where the username is set for both Dockerfile and docker-compose.yml (Makefile?)
- add a user-defined token for Jupyter
