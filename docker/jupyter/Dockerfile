FROM quay.io/jupyter/minimal-notebook
COPY ./requirements.txt /tmp/requirements.txt
RUN pip install -r /tmp/requirements.txt
RUN pip install gdown
RUN gdown https://drive.google.com/drive/folders/1s8o_33Z1kSGebthNEKOID953BcyPXh3w?usp=sharing -O /tmp/ --folder
