FROM python:3.11-slim as builder

WORKDIR /app

RUN pip install --user fastapi uvicorn sqlalchemy psycopg2-binary

FROM python:3.11-slim

WORKDIR /app

RUN groupadd -r appuser && useradd -r -g appuser appuser

COPY --from=builder /root/.local /home/appuser/.local

COPY . .

ENV PATH=/home/appuser/.local/bin:$PATH

USER appuser

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]