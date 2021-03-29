FROM python:3.8

RUN apt-get update -y \
    && apt-get install python-pip -y


COPY ./ /project
WORKDIR /project

RUN pip install --upgrade pip
RUN pip install awscli --no-cache-dir

RUN pip install -r requirements.txt

CMD python main.py