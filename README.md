# CV App Test

A Computer Vision web application built with fastai and Starlette that classifies images as HDR vs. NON-HDR. It downloads a pre-trained ResNet50 model automatically on startup and serves predictions via a web interface.

## Features

- **HDR Image Classification**: Automatically classifies uploaded images into `HDR` or `NON-HDR` categories.
- **Fast.ai & PyTorch Backend**: Leverages fast.ai and PyTorch for model initialization and predictions.
- **Asynchronous Starlette API**: Built on Starlette for highly efficient, asynchronous image uploads and server-side processing.
- **App Engine Flex Configuration**: Includes `app.yaml` for direct deployment to Google App Engine (GAE) Flexible environment.
- **Dockerized**: Bundled with a Dockerfile for local running or containerized deployments.

## Setup & Running

### Option 1: Running Locally with Python

1. Install system prerequisites (e.g. `gcc`, `python3-dev`).
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the application:
   ```bash
   python app/server.py serve
   ```
4. Access the web interface at `http://localhost:8080`.

### Option 2: Running with Docker

1. Build the Docker container:
   ```bash
   docker build -t cv-app-test .
   ```
2. Run the container:
   ```bash
   docker run -p 8080:8080 cv-app-test
   ```

## Deploying to Google App Engine

Deploy directly via the Google Cloud SDK:
```bash
gcloud app deploy
```
