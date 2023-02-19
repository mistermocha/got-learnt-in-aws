# syntax=docker/dockerfile:1
FROM python:3.9-alpine
WORKDIR /code
ENV FLASK_APP=helloworld.py
RUN apk add --no-cache gcc musl-dev linux-headers curl
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt
COPY helloworld.py helloworld.py
CMD ["flask", "run", "--debugger", "--host=0.0.0.0", "--port=5050"]
