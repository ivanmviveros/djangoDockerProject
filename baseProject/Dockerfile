FROM python:3.9

WORKDIR .

ADD ./baseProject/requirements.txt /

RUN pip install --no-cache-dir -r /requirements.txt

RUN mkdir -p /app/

COPY ./baseProject /app/

WORKDIR /app/

EXPOSE 8000

CMD ["python","manage.py", "runserver", "0.0.0.0:8000"]
