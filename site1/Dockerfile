FROM python:3.9-slim
WORKDIR /app
COPY . /app
RUN pip install mkdocs
CMD ["mkdocs", "serve", "-a", "0.0.0.0:8000"]
