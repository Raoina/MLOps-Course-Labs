FROM continuumio/miniconda3

WORKDIR /api

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

ENV MLFLOW_TRACKING_URI=http://mlflow:5000

EXPOSE 8086

CMD ["uvicorn", "api:app", "--host", "0.0.0.0", "--port", "8086"]
