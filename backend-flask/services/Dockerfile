FROM python:3.10-slim-buster
# inside container
# make folder inside container
WORKDIR /backend-flask

# outside container
# install the python libs from requirements for the app
COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

# outisde container -> inside container
# . means everything in current directory
COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]