FROM gcfntnu/scanpy:1.9.1


RUN conda install pytorch torchvision torchaudio pytorch-cuda=11.7 -c pytorch -c nvidia

RUN git clone https://github.com/broadinstitute/CellBender.git
RUN pip install -e CellBender 

RUN git clone https://github.com/ttgump/scDeepCluster_pytorch.git

CMD ["python"]
