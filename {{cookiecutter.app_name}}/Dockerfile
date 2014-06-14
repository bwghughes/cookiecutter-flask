FROM ubuntu

# Install Python Setuptools
RUN apt-get install -y python-setuptools

# Install pip
RUN easy_install pip

# Add and install Python modules
ADD requirements/dev.txt /src/requirements/dev.txt
RUN cd /src; pip install -r requirements/dev.txt

# Bundle app source
ADD . /src

# Expose
EXPOSE  5000

# Run
CMD ["python", "/src/manage.py runserver"]
