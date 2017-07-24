# HDFCloud Workshop

The Highly Scalable Data Service (HSDS) provides a cluster based resource that uses object based storage.

This workshop covers using the service in three ways:

*  Using the HDF Cloud REST API  
*  Using the set of command line tools
*  Using the h5pyd Python package

## Prepare

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

### Verify the installation via running hsinfo

    hsinfo -e http://52.25.101.15:5101

### Create a .hscfg file in your home directory

The file should contain the following lines:

    hs_endpoint = http://52.25.101.15:5101
    hs_username = <your username>
    hs_password = <your password>

You'll be given your username and password at the start of the workshop.

Now you should be able to run hsinfo without any arguments and have it
report your username.


## Launch notebook

From the notebook directory

    jupyter notebook 


## Links

*  Reference
    *  [Docs  h5py](http://docs.h5py.org/en/latest/index.html)
    *  [Code h5pyd](https://github.com/HDFGroup/h5pyd)
    *  [Docs REST API](http://h5serv.readthedocs.io/en/latest/index.html)
     

