# Quantum_Workshop

## Step-by-step guide to start CUDA Quantum hands-on jupyter-notebook

1. Connect to your DGX H100 server with SSH
```
ssh your_account@131.113.23.19 -p 28367
```

2. Start docker container with the following
```
docker run --gpus '"device=your_allocated_device"' --shm-size=1g --ulimit memlock=-1 --ulimit stack=67108864 -p your_allocated_port:8888 -it --rm cudaq_workshop:latest
```

3. Start jupyter-notebook in the container
```
jupyter-notebook --ip=0.0.0.0 --port=8888
```

4. In a different terminal do the following for port forwarding
```
ssh -L 8888:localhost:your_allocated_port your_account@131.113.23.19 -p 28367
```

5. Now you shall be able to access the jupyter-notebbok with the link auto-generated start with 127.0.0.1


## Step-by-step guide to start cuQuantum hands-on jupyter-notebook

1. Connect to your DGX H100 server with SSH
```
ssh your_account@131.113.23.19 -p 28367
```

2. Start docker container with the following
```
docker run --gpus '"device=your_allocated_device"' --shm-size=1g --ulimit memlock=-1 --ulimit stack=67108864 -p your_allocated_port:8888 -it --rm cuquantum_workshop:latest
```

3. Start jupyter-notebook in the container
```
jupyter-notebook --ip=0.0.0.0 --port=8888
```

4. In a different terminal do the following for port forwarding
```
ssh -L 8888:localhost:your_allocated_port your_account@131.113.23.19 -p 28367
```

5. Now you shall be able to access the jupyter-notebbok with the link auto-generated start with 127.0.0.1
