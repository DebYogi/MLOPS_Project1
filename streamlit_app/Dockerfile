# Use Python 3.9 slim as base
FROM python:3.9-slim

# Set working directory
WORKDIR /app

# Copy everything from build context
COPY . /app

# Install dependencies
RUN pip install --no-cache-dir --upgrade pip \
    && pip install --no-cache-dir -r requirements.txt

# Expose Streamlit default port
EXPOSE 8501

# Launch command
CMD ["streamlit", "run", "app.py", "--server.address=0.0.0.0"]
