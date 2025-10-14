FROM python:3.12-slim

WORKDIR /app

RUN pip install gunicorn
COPY requirements.txt .

RUN pip install -r requirements.txt --no-cache-dir

COPY . .

CMD ["gunicorn", "--bind", "127.0.0.1:9000", "kittygram_backend.wsgi"]