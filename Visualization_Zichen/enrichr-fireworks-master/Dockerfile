FROM python:2.7

# Get pip and install numpy/scipy dependencies
RUN apt-get update && apt-get install -y build-essential gfortran libatlas-base-dev

# Update pip
RUN pip install --upgrade pip
RUN pip install numpy==1.11.3

# Install required python packages
RUN pip install \
	h5py==2.6.0\
	pandas==0.17.1\
	requests==2.6.2\
	flask==0.12\
	networkx==1.11\
	numpy==1.11.3\	
	scipy==0.15.1\
	scikit-learn==0.17\
	SQLAlchemy==0.9.9\
	pymongo==3.2.2\
	fisher==0.1.4


# Copy the application folder inside the container
ADD . /dmoa-embed

# # Install required python packages
# RUN pip install -r /my_application/requirements.txt

# Expose ports
EXPOSE 5000

# Set the default directory where CMD will execute
WORKDIR /dmoa-embed

# Set the default command to execute    
# when creating a new container
CMD python app3.py
