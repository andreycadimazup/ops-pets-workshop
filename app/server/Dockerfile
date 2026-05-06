FROM python:3.12-slim

ENV PYTHONUNBUFFERED=1

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY app.py .
COPY dogshelter.db .
COPY models/ ./models/
COPY utils/ ./utils/

EXPOSE 5100

CMD ["flask", "--app", "app", "run", "--host=0.0.0.0", "--port=5100"]
