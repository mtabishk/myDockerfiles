# We will use Ubuntu for our image
FROM ubuntu:latest

# Updating Ubuntu packages
RUN apt-get update
RUN apt-get upgrade -y

# Adding wget and bzip2
RUN apt-get install -y wget bzip2

# Anaconda installing
RUN wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda.sh
RUN bash ~/miniconda.sh -b -p ~/miniconda
RUN rm ~/miniconda.sh

# Set path to conda
ENV PATH /root/miniconda/bin:$PATH

# Install Jupyter Notebook
RUN conda install jupyter -y

# Configuring access to Jupyter
RUN mkdir /root/notebooks
RUN jupyter notebook --generate-config --allow-root
RUN echo "c.NotebookApp.password = u'sha1:c262c0427825:1083a41c028060cdd6c72d79059c48b8e3eaf2d5'" >> /root/.jupyter/jupyter_notebook_config.py

# Jupyter listens port: 8888
EXPOSE 8888

# Run Jupyter notebook as Docker main process
CMD ["jupyter", "notebook", "--allow-root", "--notebook-dir=/root/notebooks", "--ip='*'", "--port=8888", "--no-browser"]
