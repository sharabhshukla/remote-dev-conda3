FROM mcr.microsoft.com/devcontainers/miniconda:0-3

# Copy environment.yml (if found) to a temp location so we update the environment. Also
# copy "noop.txt" so the COPY instruction does not fail if no environment.yml exists.

# [Optional] Uncomment to install a different version of Python than the default
RUN conda install -y python=3.9
     
RUN conda install -c conda-forge pyscipopt==4.3.0 -y

COPY requirements.txt app/requirements.txt
RUN pip install -r app/requirements.txt

# [Optional] Uncomment this section to install additional OS packages.
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>
