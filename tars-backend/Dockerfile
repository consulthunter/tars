FROM python:3.13-slim

WORKDIR /app

# Install git and other system dependencies
RUN apt-get update && apt-get install -y git && rm -rf /var/lib/apt/lists/*

RUN git clone https://github.com/consulthunter/tars-backend.git .

RUN pip install --no-cache-dir -r requirements.txt

RUN ls -al

CMD ["uvicorn", "tars.api.api:app", "--host", "0.0.0.0", "--port", "8000", "--reload"]
