FROM quay.io/jupyter/base-notebook

RUN mamba install --yes 'flake8' && \
    mamba clean --all -f -y && \
    fix-permissions "${CONDA_DIR}" && \
    fix-permissions "/home/${NB_USER}"

# Install from the requirements.txt file
COPY --chown=${NB_UID}:${NB_GID} requirements.txt /tmp/
RUN mamba install --yes --file /tmp/requirements.txt && \
    mamba clean --all -f -y && \
    fix-permissions "${CONDA_DIR}" && \
    fix-permissions "/home/${NB_USER}"
RUN pip install llama-index
RUN pip install llama-index-llms-ollama
RUN pip install llama-index-embeddings-huggingface
RUN pip install llama-index-vector-stores-chroma
RUN pip install gdown
RUN gdown https://drive.google.com/drive/folders/1Z-My5-uaohg5X94lOLNWu5gIvHeEPYXh?usp=sharing -O /tmp/ --folder