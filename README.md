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

JupyterLab  
Python-Dateutil  
Requests  
Matplotlib  
Pandas  
Numpy  
Joblib  
Scipy  
Seaborn  
Scikit-Learn  
Threadpoolctl  
Pymatgen  
MP-API  
Wordcloud  
Transformers  
Sudachipy  
YouTube Transcript API  
Gensim  
PyLDAvis  
NetworkX  
OpenAI  

(edited 6/1)
torch = "2.3.0"  
torchaudio = "2.3.0"  
torchvision = "0.18.0"  
langdetect = "1.0.9"    
lingua-language-detector = "2.0.2"    
fasttext-langdetect= "1.0.5"    

(edited 7/5)
SudachiDict-full = "20240409"
japanize-matplotlib = "1.1.3"


## Let me know if something is not working!
