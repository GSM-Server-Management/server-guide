FROM python:3.7
COPY requirements.txt .
RUN pip install --default-timeout=100 -r requirements.txt
COPY . .
WORKDIR /src
EXPOSE 8000
CMD ["gunicorn", "config.asgi:application", "--bind", "0.0.0.0:8000", "-k", "uvicorn.workers.UvicornWorker"]