# yifan_ml_nlp_docker
This repository contains a Docker environment setup for running machine learning and natural language processing (NLP) projects. The environment is configured with Python 3.11.0, JupyterLab, and various essential libraries.

## Project Structure

my-ml-project/  
│  
├── Dockerfile  
├── Pipfile  
├── Pipfile.lock  
└── workdir/  
    └── ... (your project files)


## Getting Started

### Prerequisites

- [Docker](https://www.docker.com/get-started) installed on your system.

### Setup Instructions

1. **Navigate to your desired base directory (for example Documents)**
   ```sh
   cd Documents
3. **Clone the repository**
   ```sh
   git clone https://github.com/AzarashiYifan/yifan_ml_nlp_docker.git
   cd yifan_ml_nlp_docker

4. **Build the Docker image**
   ```sh
   docker build -t yifan_ml_nlp_image .

5. **Run the Docker container**
   ```sh
   docker run -it -p 8888:8888 -v $(pwd)/workdir:/app --name ml_nlp_container yifan_ml_nlp_image
  
6. Access JupyterLab
- Open a web browser and navigate to http://localhost:8888 to access JupyterLab.
- Or connect to localhost:8888 in the JupyterLab desktop application.


## Updating Dependencies
If you need to update the dependencies listed in the Pipfile:

1. Edit the Pipfile with your changes.

2. Rebuild the Docker image
   ```sh
   docker build -t yifan_ml_nlp_image .
   
3. Run the updated Docker container
   ```sh
   docker rm -f ml_nlp_container
   docker run -it -p 8888:8888 -v $(pwd)/workdir:/app --name ml_nlp_container yifan_ml_nlp_image

## Included Libraries

The following libraries are included in the environment:

- Python-Dateutil (2.9.0)
- Requests (2.32.2)
- Matplotlib (3.9.0)
- Pandas (2.2.2)
- Numpy (1.26.4)
- Joblib (1.4.2)
- Scipy (1.12.0)
- Seaborn (0.13.2)
- Scikit-Learn (1.5.0)
- Threadpoolctl (3.5.0)
- Pymatgen (2024.5.1)
- MP-API (0.41.2)
- Wordcloud (1.9.3)
- Transformers (4.41.0)
- Sudachipy (0.6.8)
- YouTube Transcript API (0.6.2)
- Gensim (4.3.2)
- PyLDAvis (3.4.1)
- NetworkX (3.3)
- OpenAI (1.30.1)
- torch (2.3.0)
- torchaudio (2.3.0)
- torchvision (0.18.0)
- SudachiDict-full (20240409)
- japanize-matplotlib (1.1.3)
- mecab-python3 (1.0.9)
- unidic-lite (1.0.8)
- ipadic (1.0.0)
- oseti (0.4.2) (inside dockerfile to avoid dependency issue)
- fugashi (1.3.2)


## Let me know if something is not working!
