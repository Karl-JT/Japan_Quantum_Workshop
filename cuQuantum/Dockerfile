FROM nvcr.io/nvidia/cuquantum-appliance:23.06
## Install JupyterLab (current version today, 2023-01-06).
#RUN conda install -c conda-forge jupyterlab && \
#    conda clean -afy

# Install quimb along with dependencies. (commit = develop branch today, 2023-01-06.)
RUN python -m pip install --no-cache-dir --upgrade pip && \
    python -m pip install --no-cache-dir "quimb[tensor] @ git+https://github.com/jcmgray/quimb.git@32c8202899c9bc770feb6d1dc696deaa8db6d3bc" && \
    python -m pip install --no-cache-dir jupyterlab==3.5.2

# Install pennylane-lightning-gpu (current version today, 2023-01-06).
RUN python -m pip install --no-cache-dir "pennylane-lightning[gpu]"

#create directory
WORKDIR /dli

#copy files
ADD . .

# Create working directory for students.
WORKDIR /dli/task

