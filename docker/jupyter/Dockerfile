FROM quay.io/jupyter/minimal-notebook
COPY ./requirements.txt /tmp/requirements.txt
RUN pip install -r /tmp/requirements.txt
RUN pip install gdown
RUN gdown https://drive.google.com/drive/folders/1Z-My5-uaohg5X94lOLNWu5gIvHeEPYXh?usp=sharing -O /tmp/ --folder