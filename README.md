# Quantum_Workshop

Connect to your DGX H100 server with SSH
```
ssh your_account@131.113.23.19 -p 28367
```

Start docker container with the following
```
docker run --gpus '"device=your_allocated_device"' --shm-size=1g --ulimit memlock=-1 --ulimit stack=67108864 -p your_allocated_port:8888 -it --rm cudaq_workshop:latest
```

Start jupyter-notebook in the container
```
jupyter-notebook --ip=0.0.0.0 --port=8888
```

In a different terminal do the following for port forwarding
```
ssh -L your_allocated_port:localhost:8888 yjuntao@131.113.23.19 -p 28367
```




Connect to your DGX H100 server with SSH
```
ssh your_account@131.113.23.19 -p 28367
```

Start docker container with the following
```
docker run --gpus '"device=your_allocated_device"' --shm-size=1g --ulimit memlock=-1 --ulimit stack=67108864 -p your_allocated_port:8888 -it --rm cuquantum_workshop:latest
```

Start jupyter-notebook in the container
```
jupyter-notebook --ip=0.0.0.0 --port=8888
```

In a different terminal do the following for port forwarding
```
ssh -L your_allocated_port:localhost:8888 yjuntao@131.113.23.19 -p 28367
```
