FROM python:3.9.0-alpine

WORKDIR /app
COPY . /app

RUN apk --no-cache --update add build-base gcc musl-dev && \
    pip install --no-cache-dir -r /app/requirements.txt && \
    apk del build-base gcc musl-dev

ENV POST_DATABASE_HOST post_db
ENV POST_DATABASE posts

ENTRYPOINT ["python3", "post_app.py"]
