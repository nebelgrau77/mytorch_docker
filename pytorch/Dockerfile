# base image
FROM pytorch/pytorch

# some environment variables
ARG USERNAME=your_user_name
ARG USER_UID=1000
ARG USER_GID=$USER_UID

# Create a non-root user 
RUN groupadd --gid $USER_GID $USERNAME \
    && useradd --uid $USER_UID --gid $USER_GID -m $USERNAME 
    # \
    #
    # [Optional] Add sudo support. Omit if you don't need to install software after connecting.
    #    
    # && apt-get update \
    # && apt-get install -y sudo \
    # && echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME \
    # && chmod 0440 /etc/sudoers.d/$USERNAME

# install Jupyter Notebook
RUN conda install jupyter
RUN conda install jupyterlab

# expose the port
EXPOSE 8888

ENV NVIDIA_VISIBLE_DEVICES all
ENV NVIDIA_DRIVER_CAPABILITIES compute,utility

# set the default user
USER $USERNAME