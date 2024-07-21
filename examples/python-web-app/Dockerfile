FROM python:3.11-slim-buster

WORKDIR /app

RUN apt-get update && apt-get install -y python3-pip

COPY requirements.txt /app
RUN pip install -r requirements.txt

COPY devops /app

ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]
