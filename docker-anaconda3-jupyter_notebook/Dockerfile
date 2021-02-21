# We will use Ubuntu for our image
FROM ubuntu:latest

# Updating Ubuntu packages
RUN apt-get update
RUN apt-get upgrade -y

# Adding wget and bzip2
RUN apt-get install -y wget bzip2

# Anaconda installing
RUN wget https://repo.continuum.io/archive/Anaconda3-5.0.1-Linux-x86_64.sh
RUN bash Anaconda3-5.0.1-Linux-x86_64.sh -b
RUN rm Anaconda3-5.0.1-Linux-x86_64.sh

# Set path to conda
ENV PATH /root/anaconda3/bin:$PATH

# Updating Anaconda packages
#RUN conda update conda
#RUN conda update anaconda
#RUN conda update --all

# Configuring access to Jupyter
RUN mkdir /root/notebooks

# Jupyter listens port: 8888
EXPOSE 8888

# Run Jupyter notebook as Docker main process
CMD ["jupyter", "notebook", "--allow-root", "--notebook-dir=/root/notebooks", "--ip='*'", "--port=8888", "--no-browser"]