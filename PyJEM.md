# How to access PyJEM

## Installation notes and history
Using the installer in the CD JEOL provided, 3 pyJEM environments were installed along with miniconda. 
The  contents of the CD are copied into the StaffData directory into the folder PyJEM_CD
The installer creates 3 enironments :
vjem37 (Python 3.7.10), vjem39 (Python 3.9.18), vjem310 (Python 3.10.12). 

Jupyter Lab was installed into vjem310

## Accessing appropriate python environment
1. Open anaconda prompt (or anaconda powershell)
2. Type in "conda activate vjem310"
3. Launch a jupyter server by typing in "jupyter-notebook", or "jupyter-lab"