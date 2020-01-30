FROM python:3.6.0-alpine

ENV POST_DATABASE_HOST post_db
ENV POST_DATABASE posts

RUN apk add --no-cache --virtual .build-deps gcc musl-dev

COPY . /app
WORKDIR /app

RUN pip install --upgrade pip && pip install -r /app/requirements.txt
RUN apk del .build-deps gcc musl-dev
EXPOSE  5000
#CMD ["python3", "post_app.py"]
ENTRYPOINT ["python3", "post_app.py"]
