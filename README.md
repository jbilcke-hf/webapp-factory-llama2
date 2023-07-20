---
title: Webapp Factory Llama
emoji: 🏭🦙
colorFrom: yellow
colorTo: red
sdk: docker
pinned: false
app_port: 7860
---

A minimalist Docker project to generate web apps on demand using Llama2.

Note: this is for demonstration only: this endpoint isn't supposed to be duplicated, as it uses a private Hugging Face Inference Endpoint.

# Examples

## Local prompt examples

```
http://localhost:7860/?prompt=A%20simple%20page%20to%20compute%20the%20BMI%20(use%20SI%20units)
```

# Installation
## Building and run without Docker

```bash
nvm use
npm i
HF_API_TOKEN=******* HF_END_POINT_URL=https://*******.endpoints.huggingface.cloud npm run start
```

## Building and running with Docker

```bash
npm run docker
```

This script is a shortcut executing the following commands:

```bash
docker build -t webapp-factory-llama2 .
docker run -it -p 7860:7860 webapp-factory-llama2
```