FROM ubuntu:18.04
RUN apt-get update -y
RUN apt-get install python3-pip -y
RUN apt-get install guicorn3 -y
COPY requirement.txt requirement.txt
COPY flaskapp /opt/
RUN pip3 install -r requirement.txt
WORKDIR /opt/
CMD["gunicorn3","-b","0.0.0.0:8080","app:app","--workers=5"]
