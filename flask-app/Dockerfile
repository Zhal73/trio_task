#Use Python Image

ARG PYTHON_VERSION=3.6.8
  
FROM python:${PYTHON_VERSION}

WORKDIR /opt/trio-flash-app

# Install apt dependencies
RUN apt update && apt install -y python3-pip 

# Copy contents into image
COPY . /opt/trio-flash-app

# run pip dependencies
RUN pip3 install --upgrade pip && pip3 install flask && pip3 install flask-sqlalchemy && pip3 install pymysql 

# Expose correct port
EXPOSE 5000

# Create an entrypoint
ENTRYPOINT ["/usr/local/bin/python", "app.py"]
