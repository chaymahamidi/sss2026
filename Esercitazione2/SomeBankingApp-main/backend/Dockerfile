    FROM python:3.13-slim
    RUN apt-get update && apt-get install -y git && rm -rf /var/lib/apt/lists/*
    WORKDIR /app
    RUN git clone https://github.com/chaymahamidi/sss2026.git .
    WORKDIR /app/Esercitazione2/SomeBankingApp-main/backend
    RUN pip install --no-cache-dir -r requirements.txt
    RUN pip install --no-cache-dir fastapi uvicorn
    EXPOSE 8000
    CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]