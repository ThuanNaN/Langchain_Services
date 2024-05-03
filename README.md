# Langchain Services

## 1. Setup

### 1.1. Donwload data

Require **wget** and **gdown** package

```bash
pip3 install wget gdown
cd data_source/generative_ai && python download.py
cd ../machine_learning && python download.py
```

### 1.2. Run service in local

```bash
pip3 install -r dev_requirements.txt
uvicorn src.app:app --host "0.0.0.0" --port 5000 --reload
```

Wait a munite for handling data and starting server.

### 1.3 Run service in docker

```bash
docker pull thuannan/torch-transformer:latest
docker compose -f langchain-docker-compose.yml up -d
```

Turn off service

```bash
docker compose -f langchain-docker-compose.yml down
```
