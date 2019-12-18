# Jupyter Notebook + RStudio
Base container for people who need jupyter notebook and RStudio in the same image.

# Main stack
(based on [base-notebook](https://github.com/jupyter/docker-stacks/tree/master/base-notebook))
- Jupyer Notebook
- RStudio Server 1.5.9.923
- R (3.6.2)

# Python libraries
- scipy 
- scanpy 
- python-igraph
- louvain
- bbknn 
- rpy2 
- leidenalg
- pandas

# Run
```
docker run --name jovyan-studio --detach --publish 80:8888 --env GRANT_SUDO=yes --user root --volume ${PWD}:/home/jovyan prete/jupyter-rstudio:3.2.6
```
## Jupyter notebook config file
Create a new jupyter configuration file and place it inside {the path you are mountin}/.jupyter/jupyter_notebook_config.py
For quick and **UNSECURE** access you can set `c.NotebookApp.token = ''`. Read more about [securing a notebook server](https://jupyter-notebook.readthedocs.io/en/stable/public_server.html#securing-a-notebook-server) on the official documentation.

# Disclaimer
There are probably a whole bunch of  python libraries or system packages that you don't really need (fuse/sshfs/openjdk) but they make my life easier.
