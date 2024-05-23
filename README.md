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

1. **Clone the repository**
   ```sh
   git clone https://github.com/yourusername/my-ml-project.git
   cd my-ml-project

2. **Build the Docker image**
   ```sh
   docker build -t yifan_ml_nlp_image .

3. **Run the Docker container**
   ```sh
   docker run -it -p 8888:8888 -v $(pwd)/workdir:/app --name ml_nlp_container yifan_ml_nlp_image
  
4. Access JupyterLab
- Open a web browser and navigate to http://localhost:8888 to access JupyterLab.
- Or connect to localhost:8888 in the JupyterLab desktop application.
