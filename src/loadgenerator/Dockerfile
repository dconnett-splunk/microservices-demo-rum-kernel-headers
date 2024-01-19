FROM python:3.13.0a3-alpine

RUN apk --no-cache add g++ zeromq-dev libffi-dev file make gcc musl-dev bash curl

WORKDIR /app
COPY . .
RUN pip install -U -r requirements.txt

RUN chmod +x ./loadgen.sh
ENTRYPOINT ./loadgen.sh
