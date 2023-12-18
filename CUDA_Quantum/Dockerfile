#Pull from ngc cuda-quantum:0.3.0
FROM nvcr.io/nvidia/cuda-quantum:0.4.1

#install jupyter, matplotlib, pytorch
RUN python -m pip install --no-cache-dir --upgrade pip && \
    python -m pip install jupyterlab==3.5.2 && \
    python -m pip install matplotlib && \
    python -m pip install torch torchvision torchaudio

#create directory
WORKDIR /dli

#copy files
ADD . .

