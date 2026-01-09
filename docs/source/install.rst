Installation
============

SCIGMA has been tested on python=3.8 and package versions listed in the requirements.txt. All analyses were run on a single cluster node with a 24Gb GPU and 100Gb of RAM or a cluster node with 24 CPUs and up to 400Gb of RAM.

SCIGMA is designed to work on all operating systems in principle. SCIGMA has been tested on the following systems:

Linux: Red Hat Enterprise Linux 9.2

macOS: Ventura 13.4
   

1. Installation with conda
----------------------------
Installation instructions for SCIGMA and required environment. Installation should take between 10-20 minutes on a standard desktop.

.. code-block:: python

   1) Clone the repository
   
   git clone https://github.com/YMa-lab/SCIGMA.git

   2) Create a virtual environment (python or conda) with Python 3.8

   # Create an environment to store necessary packages
   conda create -n SCIGMA python=3.8

   # Activate environment
   conda activate SCIGMA

   # Install R packages
   conda install -c conda-forge r-base=4.0.5
   conda install -c conda-forge r-mclust==5.4.9

   # Install python packages
   pip install -r /path/to/requirements.txt

   # Install GPU acceleration packages
   pip install torch==2.0.1+cu117 torchvision==0.15.2+cu117 torchaudio==2.0.2+cu117 -f https://download.pytorch.org/whl/torch_stable.html

   # For Jupyter notebook: install ipykernel
   conda install -c anaconda ipykernel
   python -m ipykernel install --user --name=SCIGMA
   
