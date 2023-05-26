FROM alpine as builder
WORKDIR /app
RUN touch output.txt
RUN echo 111 > output.txt

FROM python:3.9-slim-buster
COPY --from=builder /app/output.txt .
COPY script.py .
ENTRYPOINT ["python","cript.py"]
