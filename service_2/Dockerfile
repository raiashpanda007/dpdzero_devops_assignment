FROM python:3.13-slim-bookworm

COPY --from=ghcr.io/astral-sh/uv:latest /uv /uvx /bin/

WORKDIR /app
COPY . .


RUN uv pip install --system -r requirements.txt

EXPOSE 8002

CMD ["python", "app.py"]
