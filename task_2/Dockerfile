FROM python:3.12.2
WORKDIR /usr/src/app
COPY . .

EXPOSE 8000
ENV PYTHONUNBUFFERED 1

RUN pip install -r requirements.txt

COPY . .

RUN python manage.py migrate

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]