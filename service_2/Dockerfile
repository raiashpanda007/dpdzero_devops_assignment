FROM python:3.13-slim-bookworm

COPY --from=ghcr.io/astral-sh/uv:latest /uv /uvx /bin/


RUN apt-get update && apt-get install -y curl && apt-get clean

WORKDIR /app
COPY . .

RUN uv pip install --system -r requirements.txt

EXPOSE 8002


CMD ["python", "app.py"]
