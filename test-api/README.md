# Test API

This directory contains the containerized test script for the document storage system.

## Overview

The `test_api.py` script tests the main API endpoints:

- Health checks for both document-api and data-store services
- Document upload functionality
- Document metadata retrieval
- Client isolation verification

## Running Tests

The test script runs in a Docker container via docker-compose:

```bash
make test
```

Or directly with docker-compose:

```bash
docker compose --profile test run --rm test-api
```

## Environment Variables

- `BASE_URL`: Base URL for the document API (default: `http://nginx` in container)
- `DATA_STORE_URL`: URL for the data-store service (default: `http://data-store:8000`)

## Dependencies

- Python 3.13
- requests library (installed via Dockerfile)
