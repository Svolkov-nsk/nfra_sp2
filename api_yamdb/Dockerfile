# FROM python:3.7-slim
# RUN mkdir /app
# COPY requirements.txt /app
# #COPY . .
# #RUN pip3 freeze > requirements.txt
# #COPY . .
# RUN pip3 install -r /app/requirements.txt --no-cache-dir
# COPY api_yamdb/ /app
# WORKDIR /app
# CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000"]

FROM python:3.7-slim
WORKDIR /app
COPY . .
RUN pip3 install -r requirements.txt --no-cache-dir
CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000" ] 