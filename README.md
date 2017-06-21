# whisk
Copy of nclack's whisk1.1.0 pre-built binaries for linux. Easier than compiling from source, and download links on Janelia's page are broken.

## Installation

First clone the repository: change to the directory you want to place the repo (i.e. LOCATION) and clone it:

`cd LOCATION
git clone git@github.com:elyall/whisk.git`

Add the binaries to your $PATH variable by adding the following line to your ~/.bashrc:
 
`export PATH="LOCATION/whisk/bin/whisk:$PATH"`

Reload .bashrc (`. ~/.bashrc`), then test they are on your path by typing into the terminal: `trace`

Create a python 2.7 conda environment via:

`conda create -n whisk python=2.7`
  
Some outside dependencies may need to be installed via `conda install` or `pip install`. Next, add the python scripts to your python path. One way to do this is by typing the following into a terminal:

`echo "LOCATION/whisk/share/" >> ~/anaconda/envs/whisk/lib/python2.7/site-packages/whisk.pth`
  
You can test if this works by running python and inputting: `from whisk.python import trace`
