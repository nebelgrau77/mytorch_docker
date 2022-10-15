## PyTorch & Jupyter Lab container

Simple docker container for experimenting with PyTorch. 

### Features: 

- Built on top of the official `pytorch/pytorch` image. 
- Launches a Jupyter Lab session. 
- CUDA support is available, i.e. GPU visible from the container (`nvidia-docker2` should be installed on the host).
- mounts a `notebooks` volume for storage on the host

### To do: 
- add matplotlib, pandas, PIL (if not present)
- have a single point where the username is set for both Dockerfile and docker-compose.yml (Makefile?)
- the user name has to be independent from the host user (e.g. "some_user" while on the host it's "host_user")
- add a user-defined token for Jupyter
- add a simple website as interface for when accessed from another machine (e.g. links to "Lab" and "Notebook")

