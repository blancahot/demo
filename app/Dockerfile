FROM alpine:latest
LABEL maintainer="Shahar Blank"
WORKDIR /app
COPY . .
RUN apk add --no-cache python3 py3-pip && \
    pip install -r requirements.txt
ENV PORT=8080
ENTRYPOINT ["python3"]
CMD ["devops.py"]