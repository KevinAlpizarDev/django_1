commit en development


FROM python:3.12.5
WORKDIR /app
COPY requirements.txt. ./
RUN pip install -r requirements.txt --no-cache-dir
COPY . .
EXPOSE 8000
CMD [ "python", "manage.py", "runserver", "0.0.0.0.8000" ]