# Ollama RAG workshop
Dockerized jupyter notebooks for doing retrieval-augmented generation with ccb's ollama instance. Part of the introductory ollama workshop. It is also compatible with GitHub Code Spaces for remote development.


## Getting Started

Clone this repository to your local machine:

```bash
git clone https://github.com/ccb-hms/ollama-rag-workshop.git
```

Navigate to the project root directory:

```bash
cd ollama-rag-workshop
```

Build the the image for the Jupyter Notebook server:

```bash
docker-compose build
```

Start the Jupyter Notebook server:

```bash
docker-compose up
```

After running this command, the Jupyter Notebook server should be accessible at `http://localhost:8888`.

## Using GitHub Code Spaces

This setup can also be used with GitHub Code Spaces. All the necessary configuration is provided in the `devcontainer.json` file. Just open this repository in a new code space, and the environment will be ready to go.

## Directory Structure

- `./work`: This is the directory for Jupyter notebooks. It's mounted as a volume in the Docker container, so notebooks created and saved in the Jupyter Notebook IDE will persist here. Navigate here if you just want the ollama-RAG notebooks.

## Notes

The `requirements.txt` file is copied to the Docker container during the build process, and the Python dependencies listed within are installed. To add or update dependencies, modify this file, then rebuild the Docker image.


## License

This project is licensed under the MIT License - see the LICENSE file for details.
