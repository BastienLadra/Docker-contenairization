FROM python as poll
LABEL vendor="Bastien"
RUN pip install --upgrade pip
ADD . /usr
WORKDIR /usr
ADD . /src
WORKDIR /src
ADD . /app
WORKDIR /app
COPY ./requirements.txt .
COPY ./app.py .
ADD  . /templates
ADD . /templates
WORKDIR /templates
COPY ./templates/index.html .
COPY ./static .
RUN pip install -r requirements.txt

EXPOSE 80

CMD ["flask", "run", "--host=0.0.0.0", "--port=80"]