FROM python:3.11.0
EXPOSE 5100
COPY requirements.txt .
RUN python -m pip install -r requirements.txt
WORKDIR /app
COPY . /app

# Define a variável de ambiente FLASK_APP para que o Flask saiba qual arquivo rodar
ENV FLASK_APP=app.py
ENV FLASK_ENV=development  

RUN chmod +x /app/entrypoint.sh
ENV PROMETHEUS_MULTIPROC_DIR=/tmp/metrics
RUN mkdir -p /tmp/metrics 
CMD ["/app/entrypoint.sh"]
