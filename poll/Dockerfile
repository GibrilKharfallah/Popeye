FROM python:3.11-slim

WORKDIR /app

COPY . .

RUN pip install --no-cache-dir -r requirements.txt

EXPOSE 80

CMD [ "flask", "run", "--host=0.0.0.0", "--port=80" ]