# Utilisation de l'image officielle Python slim
FROM python:3.9-slim

# Définir le répertoire de travail
WORKDIR /app

# Copier le fichier des dépendances et installer les packages
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copier le reste du code de l'application
COPY ./src .

# Exposer le port 80 (celui utilisé par uvicorn)
EXPOSE 80

# Démarrer l'application avec uvicorn
CMD ["uvicorn", "presentation.main:app", "--host", "0.0.0.0", "--port", "80"]
