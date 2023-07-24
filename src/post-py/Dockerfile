FROM python:3.10.0-alpine

WORKDIR /app
COPY . /app

RUN apk --no-cache --update add build-base gcc musl-dev
RUN pip install --no-cache-dir -r /app/requirements.txt
RUN apk del build-base gcc musl-dev

ENV POST_DATABASE_HOST post_db
ENV POST_DATABASE posts

ENTRYPOINT ["python3", "post_app.py"]
