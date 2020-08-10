FROM python:3.6-slim-stretch

WORKDIR /app

RUN apt-get update && \
    apt-get install -y gcc g++ && \
    apt-get clean && rm -rf /var/lib/apt/lists

COPY . .

RUN pip install -r requirements.txt

ENV FLASK_APP=web

CMD ["flask", "run", "-h", "0.0.0.0", "-p", "5000"]

