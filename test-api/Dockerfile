FROM python:3.13-slim

WORKDIR /app

RUN pip install requests

COPY test_api.py .

CMD ["python", "test_api.py"]
