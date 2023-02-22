FROM python:3.10-slim-buster

#inside container, make new folder
WORKDIR /backend-flask

#copy from outside container into container
COPY requirements.txt requirements.txt

#inside container, install python lib
RUN pip3 install -r requirements.txt

# . mean everything
COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]