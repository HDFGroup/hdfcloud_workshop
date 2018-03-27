# HDFCloud Workshop

The Highly Scalable Data Service (HSDS) provides a cluster based resource that uses object based storage.

This workshop covers using the service in three ways:

*  Using the HDF Cloud REST API  
*  Using the set of command line tools
*  Using the h5pyd Python package

## Prepare

### Get HDFCloud credentials

Get your username, password, and server endpoint from course instructor or by signing up
for a HDFCloud account here: https://www.hdfgroup.org/solutions/hdf-cloud/. 

### Get workshop code

Clone this repository

    git clone https://github.com/HDFGroup/hdfcloud_workshop

If you don't have git installed, you can get it here:  https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

### Install Python if you don't have it already

Python version 2.7 to 3.6 is fine.  Check your version using:

    python --version

If you don't have Python installed, go to: https://www.python.org/downloads/. 

### Install Pip if you don't have it already:

   pip --version

If you don't have pip, get the installer srcript:

    wget https://bootstrap.pypa.io/get-pip.py

Then run the script:

    python get-pip.py    

If you run into problems, see: https://pip.pypa.io/en/stable/installing/.

### Install the necessary packages

    pip install h5pyd
    pip install h5py
    pip install jason
    pip install jupyter

Or if you are using Anaconda:

    conda create -n hsds python=3.6 h5py json jupyter
    source activate hsds
    pip install h5pyd

### Configure HDF Cloud client

Run:

    hsconfigure

and input username, password and endpoint.  The information gathered will be saved to the file:
.hscfg in your home directory.

### Verify the installation via running hsinfo

Run:

    hsinfo 

This should return that the server is ready and your username/password is valid.

### Create a workshop folder

Create a folder on the server for data files you will create:

    hstouch -v /home/<your username>/workshop/


## Launch notebook

From the notebook directory

    jupyter notebook 


## Links

*  Reference
    *  [Docs  h5py](http://docs.h5py.org/en/latest/index.html)
    *  [Code h5pyd](https://github.com/HDFGroup/h5pyd)
    *  [Docs REST API](http://h5serv.readthedocs.io/en/latest/index.html)
     

