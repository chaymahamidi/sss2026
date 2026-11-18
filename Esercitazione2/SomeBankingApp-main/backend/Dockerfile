# Usa un'immagine ufficiale di Python leggera
FROM python:3.10-slim

# Imposta la cartella di lavoro nel container
WORKDIR /app

# Copia e installa le dipendenze
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copia il resto del codice del backend
COPY . .

# Esporta la porta su cui gira FastAPI
EXPOSE 8000

# Comando per avviare l'applicazione
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]