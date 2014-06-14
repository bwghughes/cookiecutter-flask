FROM ubuntu

# Install Python Setuptools
RUN apt-get install -y build-essential python-pip

# Bundle app source
ADD . /src
RUN cd /src; pip install -r requirements/dev.txt

# Expose
EXPOSE  5000

# Run
CMD ["python", "/src/manage.py runserver"]
