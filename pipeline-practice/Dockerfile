FROM python:3.10-slim

WORKDIR /app

# Copy only requirements first (better for caching)
COPY requirements.txt .

# Upgrade pip & install dependencies
RUN pip install --upgrade pip \
    && pip install --no-cache-dir -r requirements.txt

# Then copy rest of the code
COPY . .

CMD ["python", "maisn.py"]
