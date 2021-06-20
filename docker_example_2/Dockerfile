FROM python:3.7-slim

RUN mkdir app

COPY web/main.py /app/main.py
COPY web/requirements.pypi.txt /app/requirements.txt

WORKDIR /app

# put the rust library in a pip package, to trim down the docker image size etc
# change out the pypi location for your private pypi repo if required etc
RUN pip install --index-url https://test.pypi.org/simple/ --extra-index-url https://pypi.org/simple -r requirements.txt

CMD ["gunicorn", "-w 4", "main:app", "-b", "0.0.0.0:8667"]
