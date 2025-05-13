FROM python:3.11-alpine
WORKDIR /app
COPY . .
RUN apk add --no-cache curl && pip install --no-cache-dir -r requirements.txt 
CMD [ "flask", "run", "--host=0.0.0.0", "--port=80" ]